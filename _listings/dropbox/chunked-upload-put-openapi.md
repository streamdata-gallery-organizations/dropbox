---
swagger: "2.0"
x-collection-name: Dropbox
x-complete: 0
info:
  title: Dropbox Content Uploads large files to Dropbox in multiple chunks.
  description: |-
    Uploads large files to Dropbox in multiple chunks. Also has the ability to resume if the upload is interrupted.
    This allows for uploads larger than the `/files_put` maximum of 150 MB.

    Typical usage:
      1. Send a PUT request to `/chunked_upload` with the first chunk of the file without setting `upload_id`, and
      receive an `upload_id` in return.
      2. Repeatedly `PUT` subsequent chunks using the `upload_id` to identify the upload in progress and an `offset`
      representing the number of bytes transferred so far.
      3. After each chunk has been uploaded, the server returns a new offset representing the total amount transferred.
      4. After the last chunk, `POST` to `/commit_chunked_upload` to complete the upload.

    Chunks can be any size up to 150 MB. A typical chunk is 4 MB. Using large chunks will mean fewer calls
    to `/chunked_upload` and faster overall throughput. However, whenever a transfer is interrupted, you will
    have to resume at the beginning of the last chunk, so it is often safer to use smaller chunks.

    If the offset you submit does not match the expected offset on the server, the server will ignore the request
    and respond with a 400 error that includes the current offset. To resume upload, seek to the correct offset
    (in bytes) within the file and then resume uploading from that point.

    A chunked upload can take a maximum of 48 hours before expiring.
  termsOfService: https://www.dropbox.com/developers/reference/tos
  contact:
    name: Dropbox
    url: https://www.dropbox.com/developers
  version: 1.0.0
host: api-content.dropbox.com
basePath: /1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /files/{root}/{path}:
    get:
      summary: Downloads a file.
      description: |-
        Downloads a file.

        This method also supports [HTTP Range Retrieval Requests](http://www.w3.org/Protocols/rfc2616/rfc2616-sec14.html#sec14.35.2)
        to allow retrieving partial file contents.
      operationId: downloads-a-filethis-method-also-supports-http-range-retrieval-requestshttpwwww3orgprotocolsrfc2616r
      x-api-path-slug: filesrootpath-get
      parameters:
      - in: path
        name: path
        description: The path to the file you want to retrieve
      - in: query
        name: rev
        description: The revision of the file to retrieve
      - in: path
        name: root
        description: 'Root folder: `auto` - automatically determines the appropriate
          root folder using your apps permissionlevel (recommended); `sandbox` - the
          codename for app folder level; `dropbox` - full dropbox access'
      responses:
        200:
          description: OK
      tags:
      - Storage
      - Documents
      - Files
      - Root
      - Path
  /files_put/{root}/{path}:
    post:
      summary: Uploads a file using PUT semantics.
      description: |-
        Uploads a file using PUT semantics.

        The preferred HTTP method for this call is **PUT**. For compatibility with browser environments, the **POST**
        HTTP method is also recognized.

        **Note:** Providing a `Content-Length` header set to the size of the uploaded file is required so that the
        server can verify that it has received the entire file contents.

        **Note:** `/files_put` has a maximum file size limit of 150 MB and does not support uploads with chunked
        encoding. To upload larger files, use [/chunked_upload](https://www.dropbox.com/developers/core/docs#chunked-upload)
        instead.
      operationId: uploads-a-file-using-put-semanticsthe-preferred-http-method-for-this-call-is-put-for-compatibility-w
      x-api-path-slug: files-putrootpath-post
      parameters:
      - in: query
        name: autorename
        description: This value, either `true` (default) or `false`, determines what
          happens when there is a conflict
      - in: body
        name: file_content
        description: The file contents to be uploaded
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: locale
        description: The metadata returned on successful upload will have its `size`
          field translated based on the given locale
      - in: query
        name: overwrite
        description: This value, either `true` (default) or `false`, determines whether
          an existing file will be overwrittenby this upload
      - in: query
        name: parent_rev
        description: If present, this parameter specifies the revision of the file
          youre editing
      - in: path
        name: path
        description: The full path to the file you want to write to
      - in: path
        name: root
        description: 'Root folder: `auto` - automatically determines the appropriate
          root folder using your apps permissionlevel (recommended); `sandbox` - the
          codename for app folder level; `dropbox` - full dropbox access'
      responses:
        200:
          description: OK
      tags:
      - Storage
      - Documents
      - Files
      - Put
      - Root
      - Path
    put:
      summary: Uploads a file using PUT semantics.
      description: |-
        Uploads a file using PUT semantics.

        The preferred HTTP method for this call is **PUT**. For compatibility with browser environments, the **POST**
        HTTP method is also recognized.

        **Note:** Providing a `Content-Length` header set to the size of the uploaded file is required so that the
        server can verify that it has received the entire file contents.

        **Note:** `/files_put` has a maximum file size limit of 150 MB and does not support uploads with chunked
        encoding. To upload larger files, use [/chunked_upload](https://www.dropbox.com/developers/core/docs#chunked-upload)
        instead.
      operationId: uploads-a-file-using-put-semanticsthe-preferred-http-method-for-this-call-is-put-for-compatibility-w
      x-api-path-slug: files-putrootpath-put
      parameters:
      - in: query
        name: autorename
        description: This value, either `true` (default) or `false`, determines what
          happens when there is a conflict
      - in: body
        name: file_content
        description: The file contents to be uploaded
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: locale
        description: The metadata returned on successful upload will have its `size`
          field translated based on the given locale
      - in: query
        name: overwrite
        description: This value, either `true` (default) or `false`, determines whether
          an existing file will be overwrittenby this upload
      - in: query
        name: parent_rev
        description: If present, this parameter specifies the revision of the file
          youre editing
      - in: path
        name: path
        description: The full path to the file you want to write to
      - in: path
        name: root
        description: 'Root folder: `auto` - automatically determines the appropriate
          root folder using your apps permissionlevel (recommended); `sandbox` - the
          codename for app folder level; `dropbox` - full dropbox access'
      responses:
        200:
          description: OK
      tags:
      - Storage
      - Documents
      - Files
      - Put
      - Root
      - Path
  /thumbnails/{root}/{path}:
    get:
      summary: Gets a thumbnail for an image.
      description: |-
        Gets a thumbnail for an image.

        This method currently supports files with the following file extensions: .jpg, .jpeg, .png, .tiff, .tif, .gif, .bmp

        Photos that are larger than 20MB in size won't be converted to a thumbnail.
      operationId: gets-a-thumbnail-for-an-imagethis-method-currently-supports-files-with-the-following-file-extensions
      x-api-path-slug: thumbnailsrootpath-get
      parameters:
      - in: query
        name: format
        description: For images that are photos, `jpeg` (default) should be preferred,
          while `png` is better for screenshots and digital art
      - in: path
        name: path
        description: The path to the image file you want to thumbnail
      - in: path
        name: root
        description: 'Root folder: `auto` - automatically determines the appropriate
          root folder using your apps permissionlevel (recommended); `sandbox` - the
          codename for app folder level; `dropbox` - full dropbox access'
      - in: query
        name: size
        description: Default size is `s`
      responses:
        200:
          description: OK
      tags:
      - Storage
      - Documents
      - Thumbnails
      - Root
      - Path
  /previews/{root}/{path}:
    get:
      summary: Gets a preview for a file.
      description: |-
        Gets a preview for a file.

        Previews are only generated for the files with the following extensions: .doc, .docx, .docm, .ppt, .pps,
        .ppsx, .ppsm, .pptx, .pptm, .xls, .xlsx, .xlsm, .rtf
      operationId: gets-a-preview-for-a-filepreviews-are-only-generated-for-the-files-with-the-following-extensions-doc
      x-api-path-slug: previewsrootpath-get
      parameters:
      - in: path
        name: path
        description: The absolute path to the file you want to preview
      - in: query
        name: rev
        description: The revision of the file to retrieve
      - in: path
        name: root
        description: 'Root folder: `auto` - automatically determines the appropriate
          root folder using your apps permissionlevel (recommended); `sandbox` - the
          codename for app folder level; `dropbox` - full dropbox access'
      responses:
        200:
          description: OK
      tags:
      - Storage
      - Documents
      - Previews
      - Root
      - Path
  /chunked_upload:
    put:
      summary: Uploads large files to Dropbox in multiple chunks.
      description: |-
        Uploads large files to Dropbox in multiple chunks. Also has the ability to resume if the upload is interrupted.
        This allows for uploads larger than the `/files_put` maximum of 150 MB.

        Typical usage:
          1. Send a PUT request to `/chunked_upload` with the first chunk of the file without setting `upload_id`, and
          receive an `upload_id` in return.
          2. Repeatedly `PUT` subsequent chunks using the `upload_id` to identify the upload in progress and an `offset`
          representing the number of bytes transferred so far.
          3. After each chunk has been uploaded, the server returns a new offset representing the total amount transferred.
          4. After the last chunk, `POST` to `/commit_chunked_upload` to complete the upload.

        Chunks can be any size up to 150 MB. A typical chunk is 4 MB. Using large chunks will mean fewer calls
        to `/chunked_upload` and faster overall throughput. However, whenever a transfer is interrupted, you will
        have to resume at the beginning of the last chunk, so it is often safer to use smaller chunks.

        If the offset you submit does not match the expected offset on the server, the server will ignore the request
        and respond with a 400 error that includes the current offset. To resume upload, seek to the correct offset
        (in bytes) within the file and then resume uploading from that point.

        A chunked upload can take a maximum of 48 hours before expiring.
      operationId: uploads-large-files-to-dropbox-in-multiple-chunks-also-has-the-ability-to-resume-if-the-upload-is-in
      x-api-path-slug: chunked-upload-put
      parameters:
      - in: body
        name: file_content
        description: A chunk of data from the file being uploaded
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: offset
        description: The byte offset of this chunk, relative to the beginning of the
          full file
      - in: query
        name: upload_id
        description: The unique ID of the in-progress upload on the server
      responses:
        200:
          description: OK
      tags:
      - Storage
      - Documents
      - Chunked
      - Upload
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---