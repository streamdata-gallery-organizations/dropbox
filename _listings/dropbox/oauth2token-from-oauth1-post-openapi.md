---
swagger: "2.0"
x-collection-name: Dropbox
x-complete: 0
info:
  title: Dropbox Core Convert OAuth 1 token to OAuth 2 token.
  description: |-
    This endpoint should be used by apps transitioning from OAuth 1 to OAuth 2. It will return an OAuth 2 token
    for the authenticated user.
  termsOfService: https://www.dropbox.com/developers/reference/tos
  contact:
    name: Dropbox
    url: https://www.dropbox.com/developers
  version: 1.0.0
host: api.dropbox.com
basePath: /1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /get_info:
    post:
      summary: Get Info
      description: Get info.
      operationId: postGetInfo
      x-api-path-slug: get-info-post
      responses:
        200:
          description: OK
      tags:
      - Info
  /log/get_events:
    post:
      summary: Get Events
      description: Get events.
      operationId: postLogGetEvents
      x-api-path-slug: logget-events-post
      parameters:
      - in: query
        name: category
        description: optional filter the returned events to a single category (see
          Event types below)
      - in: query
        name: cursor
        description: optional encoded value indicating from what point to get the
          next limit logs
      - in: query
        name: end_ts
        description: optional end time (UTC timestamp in milliseconds since the Unix
          epoch)
      - in: query
        name: limit
        description: optional number of results to return per call (default 1000,
          maximum 1000)
      - in: query
        name: start_ts
        description: optional start time (UTC timestamp in milliseconds since the
          Unix epoch)
      - in: query
        name: user
        description: optional member ID, user ID, or email of a user for filtering
          events
      responses:
        200:
          description: OK
      tags:
      - Events
  /members/add:
    post:
      summary: Add Member
      description: Add member.
      operationId: postMembersAdd
      x-api-path-slug: membersadd-post
      parameters:
      - in: query
        name: member_email
        description: member email
      - in: query
        name: member_external_id
        description: optional external ID for member
      - in: query
        name: member_given_name
        description: member first name
      - in: query
        name: member_surname
        description: member last name
      - in: query
        name: send_welcome_email
        description: optional boolean to send a welcome email to the member
      responses:
        200:
          description: OK
      tags:
      - Member
  /members/get_info:
    post:
      summary: Get Member Info
      description: Get member info.
      operationId: postMembersGetInfo
      x-api-path-slug: membersget-info-post
      parameters:
      - in: query
        name: email
        description: optional email of member
      - in: query
        name: external_id
        description: optional external ID of member
      - in: query
        name: member_id
        description: optional ID of member
      responses:
        200:
          description: OK
      tags:
      - Member
      - Info
  /members/get_info_batch:
    post:
      summary: Get Info Batch
      description: Get info batch.
      operationId: postMembersGetInfoBatch
      x-api-path-slug: membersget-info-batch-post
      parameters:
      - in: query
        name: emails
        description: optional list of member emails
      - in: query
        name: external_ids
        description: optional list of external member IDs
      - in: query
        name: member_ids
        description: optional list of member IDs
      responses:
        200:
          description: OK
      tags:
      - Info
      - Batch
  /members/list:
    post:
      summary: List Members
      description: List members.
      operationId: postMembersList
      x-api-path-slug: memberslist-post
      parameters:
      - in: query
        name: cursor
        description: optional encoded value indicating from what point to get the
          next limit members
      - in: query
        name: limit
        description: optional number of results to return per call (default 1000,
          maximum 1000)
      responses:
        200:
          description: OK
      tags:
      - List
      - Members
  /members/remove:
    post:
      summary: Remove
      description: Remove.
      operationId: postMembersRemove
      x-api-path-slug: membersremove-post
      parameters:
      - in: query
        name: delete_data
        description: optional controls if the users data will be deleted on their
          linked devices
      - in: query
        name: external_id
        description: optional external ID
      - in: query
        name: member_id
        description: optional member ID
      - in: query
        name: transfer_admin_member_id
        description: optional errors during the transfer process will be sent via
          email to the transfer_admin_member_id
      - in: query
        name: transfer_dest_member_id
        description: optional files from the deleted member account will be transferred
          to this member
      responses:
        200:
          description: OK
      tags:
      - Remove
  /members/set_permissions:
    post:
      summary: Set Member Permissions
      description: Set member permissions.
      operationId: postMembersSetPermissions
      x-api-path-slug: membersset-permissions-post
      parameters:
      - in: query
        name: external_id
        description: optional external ID
      - in: query
        name: member_id
        description: optional member ID
      - in: query
        name: new_is_admin
        description: optional change the admin status of the member
      responses:
        200:
          description: OK
      tags:
      - Set
      - Member
      - Permissions
  /members/set_profile:
    get:
      summary: Set Profile
      description: Set profile.
      operationId: getMembersSetProfile
      x-api-path-slug: membersset-profile-get
      parameters:
      - in: query
        name: external_id
        description: optional external ID
      - in: query
        name: member_id
        description: optional member ID
      - in: query
        name: new_email
        description: optional new email for member
      - in: query
        name: new_external_id
        description: optional new external ID for member
      - in: query
        name: new_given_name
        description: optional new given name for member
      - in: query
        name: new_surname
        description: optional new surname for member
      responses:
        200:
          description: OK
      tags:
      - Set
      - Profile
  /reports/get_activity:
    post:
      summary: Get Activity
      description: Get activity.
      operationId: postReportsGetActivity
      x-api-path-slug: reportsget-activity-post
      parameters:
      - in: query
        name: end_date
        description: optional ending date (exclusive)
      - in: query
        name: start_date
        description: optional starting date (inclusive)
      responses:
        200:
          description: OK
      tags:
      - Activity
  /reports/get_devices:
    post:
      summary: Get Devices
      description: Get devices.
      operationId: postReportsGetDevices
      x-api-path-slug: reportsget-devices-post
      parameters:
      - in: query
        name: end_date
        description: optional ending date (exclusive)
      - in: query
        name: start_date
        description: optional starting date (inclusive)
      responses:
        200:
          description: OK
      tags:
      - Devices
  /reports/get_membership:
    post:
      summary: Get Membership
      description: Get membership.
      operationId: postReportsGetMembership
      x-api-path-slug: reportsget-membership-post
      parameters:
      - in: query
        name: end_date
        description: optional ending date (exclusive)
      - in: query
        name: start_date
        description: optional starting date (inclusive)
      responses:
        200:
          description: OK
      tags:
      - Membership
  /reports/get_storage:
    post:
      summary: Get Storage
      description: Get storage.
      operationId: postReportsGetStorage
      x-api-path-slug: reportsget-storage-post
      parameters:
      - in: query
        name: end_date
        description: optional ending date (exclusive)
      - in: query
        name: start_date
        description: optional starting date (inclusive)
      responses:
        200:
          description: OK
      tags:
      - Storage
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
  /commit_chunked_upload/{root}/{path}:
    post:
      summary: Completes an upload initiated by the chunked upload method.
      description: |-
        Completes an upload initiated by the `/chunked_upload` method. Saves a file uploaded via `/chunked_upload` to
        a user's Dropbox.

        `/commit_chunked_upload` is similar to `/files_put`. The main difference is that while `/files_put` takes the
        file contents in the request body, `/commit_chunked_upload` takes a parameter `upload_id`, which is obtained
        when the file contents are uploaded via `/chunked_upload`.
      operationId: completes-an-upload-initiated-by-the-chunked-upload-method-saves-a-file-uploaded-via-chunked-upload-
      x-api-path-slug: commit-chunked-uploadrootpath-post
      parameters:
      - in: query
        name: autorename
        description: This value, either `true` (default) or `false`, determines what
          happens when there is a conflict
      - in: query
        name: locale
        description: The metadata returned on successful upload will have its `size`
          field translated based on the given locale
      - in: query
        name: overwrite
        description: This value, either `true` (default) or `false`, determines whether
          an existing file will be overwritten bythis upload
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
      - in: query
        name: upload_id
        description: Used to identify the chunked upload session youd like to commit
      responses:
        200:
          description: OK
      tags:
      - Storage
      - Documents
      - Commit
      - Chunked
      - Upload
      - Root
      - Path
  /oauth2/token_from_oauth1:
    post:
      summary: Convert OAuth 1 token to OAuth 2 token.
      description: |-
        This endpoint should be used by apps transitioning from OAuth 1 to OAuth 2. It will return an OAuth 2 token
        for the authenticated user.
      operationId: this-endpoint-should-be-used-by-apps-transitioning-from-oauth-1-to-oauth-2-it-will-return-an-oauth-2
      x-api-path-slug: oauth2token-from-oauth1-post
      responses:
        200:
          description: OK
      tags:
      - Storage
      - Documents
      - Oauth2
      - Token_from_oauth1
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