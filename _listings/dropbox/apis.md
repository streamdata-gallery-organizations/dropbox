---
name: Dropbox
x-slug: dropbox
description: Dropbox is a file hosting service operated by Dropbox, Inc., that offers
  cloud storage, file synchronization, and client software. Dropbox allows users to
  create a special folder on each of their computers, which Dropbox then synchronizes
  so that it appears to be the same folder (with the same contents) regardless of
  which computer is used to view it. Files placed in this folder also are accessible
  through a website and mobile phone applications.
image: https://avatars.githubusercontent.com/u/559357?v=3
x-kinRank: "10"
x-alexaRank: ""
tags: Dropbox
created: "2018-05-21"
modified: "2018-05-21"
url: https://raw.githubusercontent.com/streamdata-gallery-organizations/dropbox/master/_listings/dropbox/apis.md
specificationVersion: "0.14"
apis:
- name: Dropbox Content Downloads a file.
  x-api-slug: dropbox-content
  description: |-
    Downloads a file.

    This method also supports [HTTP Range Retrieval Requests](http://www.w3.org/Protocols/rfc2616/rfc2616-sec14.html#sec14.35.2)
    to allow retrieving partial file contents.
  image: https://avatars.githubusercontent.com/u/559357?v=3
  humanURL: https://www.dropbox.com
  baseURL: https://api-content.dropbox.com//1//files/{root}/{path}
  tags: Storage,Documents,Files,Root,Path
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/dropbox/master/_listings/dropbox/filesrootpath-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/dropbox/master/_listings/dropbox/filesrootpath-get-openapi.md
- name: Dropbox Content Uploads a file using PUT semantics.
  x-api-slug: dropbox-content
  description: |-
    Uploads a file using PUT semantics.

    The preferred HTTP method for this call is **PUT**. For compatibility with browser environments, the **POST**
    HTTP method is also recognized.

    **Note:** Providing a `Content-Length` header set to the size of the uploaded file is required so that the
    server can verify that it has received the entire file contents.

    **Note:** `/files_put` has a maximum file size limit of 150 MB and does not support uploads with chunked
    encoding. To upload larger files, use [/chunked_upload](https://www.dropbox.com/developers/core/docs#chunked-upload)
    instead.
  image: https://avatars.githubusercontent.com/u/559357?v=3
  humanURL: https://www.dropbox.com
  baseURL: https://api-content.dropbox.com//1//files_put/{root}/{path}
  tags: Storage,Documents,Files,Put,Root,Path
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/dropbox/master/_listings/dropbox/files-putrootpath-post-openapi.md
- name: Dropbox Content Uploads a file using PUT semantics.
  x-api-slug: dropbox-content
  description: |-
    Uploads a file using PUT semantics.

    The preferred HTTP method for this call is **PUT**. For compatibility with browser environments, the **POST**
    HTTP method is also recognized.

    **Note:** Providing a `Content-Length` header set to the size of the uploaded file is required so that the
    server can verify that it has received the entire file contents.

    **Note:** `/files_put` has a maximum file size limit of 150 MB and does not support uploads with chunked
    encoding. To upload larger files, use [/chunked_upload](https://www.dropbox.com/developers/core/docs#chunked-upload)
    instead.
  image: https://avatars.githubusercontent.com/u/559357?v=3
  humanURL: https://www.dropbox.com
  baseURL: https://api-content.dropbox.com//1//files_put/{root}/{path}
  tags: Storage,Documents,Files,Put,Root,Path
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/dropbox/master/_listings/dropbox/files-putrootpath-put-openapi.md
- name: Dropbox Content Gets a thumbnail for an image.
  x-api-slug: dropbox-content
  description: |-
    Gets a thumbnail for an image.

    This method currently supports files with the following file extensions: .jpg, .jpeg, .png, .tiff, .tif, .gif, .bmp

    Photos that are larger than 20MB in size won't be converted to a thumbnail.
  image: https://avatars.githubusercontent.com/u/559357?v=3
  humanURL: https://www.dropbox.com
  baseURL: https://api-content.dropbox.com//1//thumbnails/{root}/{path}
  tags: Storage,Documents,Thumbnails,Root,Path
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/dropbox/master/_listings/dropbox/thumbnailsrootpath-get-openapi.md
- name: Dropbox Content Gets a preview for a file.
  x-api-slug: dropbox-content
  description: |-
    Gets a preview for a file.

    Previews are only generated for the files with the following extensions: .doc, .docx, .docm, .ppt, .pps,
    .ppsx, .ppsm, .pptx, .pptm, .xls, .xlsx, .xlsm, .rtf
  image: https://avatars.githubusercontent.com/u/559357?v=3
  humanURL: https://www.dropbox.com
  baseURL: https://api-content.dropbox.com//1//previews/{root}/{path}
  tags: Storage,Documents,Previews,Root,Path
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/dropbox/master/_listings/dropbox/previewsrootpath-get-openapi.md
- name: Dropbox Content Uploads large files to Dropbox in multiple chunks.
  x-api-slug: dropbox-content
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
  image: https://avatars.githubusercontent.com/u/559357?v=3
  humanURL: https://www.dropbox.com
  baseURL: https://api-content.dropbox.com//1//chunked_upload
  tags: Storage,Documents,Chunked,Upload
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/dropbox/master/_listings/dropbox/chunked-upload-put-openapi.md
- name: Dropbox Content Completes an upload initiated by the chunked upload method.
  x-api-slug: dropbox-content
  description: |-
    Completes an upload initiated by the `/chunked_upload` method. Saves a file uploaded via `/chunked_upload` to
    a user's Dropbox.

    `/commit_chunked_upload` is similar to `/files_put`. The main difference is that while `/files_put` takes the
    file contents in the request body, `/commit_chunked_upload` takes a parameter `upload_id`, which is obtained
    when the file contents are uploaded via `/chunked_upload`.
  image: https://avatars.githubusercontent.com/u/559357?v=3
  humanURL: https://www.dropbox.com
  baseURL: https://api-content.dropbox.com//1//commit_chunked_upload/{root}/{path}
  tags: Storage,Documents,Commit,Chunked,Upload,Root,Path
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/dropbox/master/_listings/dropbox/commit-chunked-uploadrootpath-post-openapi.md
- name: Dropbox Content
  x-api-slug: dropbox-content
  description: Dropbox is a file hosting service operated by Dropbox, Inc., that offers
    cloud storage, file synchronization, and client software. Dropbox allows users
    to create a special folder on each of their computers, which Dropbox then synchronizes
    so that it appears to be the same folder (with the same contents) regardless of
    which computer is used to view it. Files placed in this folder also are accessible
    through a website and mobile phone applications.
  image: https://avatars.githubusercontent.com/u/559357?v=3
  humanURL: https://www.dropbox.com
  baseURL: https://api-content.dropbox.com//1
  tags: Dropbox
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/dropbox/master/_listings/dropbox/openapi.md
- name: Dropbox Core Convert OAuth 1 token to OAuth 2 token.
  x-api-slug: dropbox-core
  description: |-
    This endpoint should be used by apps transitioning from OAuth 1 to OAuth 2. It will return an OAuth 2 token
    for the authenticated user.
  image: https://avatars.githubusercontent.com/u/559357?v=3
  humanURL: https://www.dropbox.com
  baseURL: https://api.dropbox.com//1//oauth2/token_from_oauth1
  tags: Storage,Documents,Oauth2,Token_from_oauth1
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/dropbox/master/_listings/dropbox/oauth2token-from-oauth1-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/dropbox/master/_listings/dropbox/oauth2token-from-oauth1-post-openapi.md
- name: Dropbox Core Disables the access token.
  x-api-slug: dropbox-core
  description: Disables the access token used to authenticate the call. This method
    works for OAuth 1 and OAuth 2 tokens.
  image: https://avatars.githubusercontent.com/u/559357?v=3
  humanURL: https://www.dropbox.com
  baseURL: https://api.dropbox.com//1//disable_access_token
  tags: Storage,Documents,Disable_access_token
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/dropbox/master/_listings/dropbox/disable-access-token-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/dropbox/master/_listings/dropbox/disable-access-token-post-openapi.md
- name: Dropbox Core Retrieves information about the user's account.
  x-api-slug: dropbox-core
  description: Retrieves information about the user's account.
  image: https://avatars.githubusercontent.com/u/559357?v=3
  humanURL: https://www.dropbox.com
  baseURL: https://api.dropbox.com//1//account/info
  tags: Storage,Documents,Account,Info
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/dropbox/master/_listings/dropbox/accountinfo-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/dropbox/master/_listings/dropbox/accountinfo-get-openapi.md
- name: Dropbox Core Retrieves file and folder metadata.
  x-api-slug: dropbox-core
  description: |-
    Retrieves file and folder metadata.

    **Note:** `modified`, `rev`, and `revision` aren't returned in the metadata for the root/top-level path.
  image: https://avatars.githubusercontent.com/u/559357?v=3
  humanURL: https://www.dropbox.com
  baseURL: https://api.dropbox.com//1//metadata/{root}/{path}
  tags: Storage,Documents,Metadata,Root,Path
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/dropbox/master/_listings/dropbox/metadatarootpath-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/dropbox/master/_listings/dropbox/metadatarootpath-get-openapi.md
- name: Dropbox Core A way of letting you keep up with changes to files and folders
    in a user's Dropbox.
  x-api-slug: dropbox-core
  description: |-
    A way of letting you keep up with changes to files and folders in a user's Dropbox.

    You can periodically call `/delta` to get a list of "delta entries", which are instructions on how to
    update your local state to match the server's state.

    If you use the `path_prefix` parameter, you must continue to pass the correct prefix on subsequent calls
    using the returned cursor. You can switch the `path_prefix` on any existing cursor to a descendant of the
    existing `path_prefix` on subsequent calls to `/delta`. For example if your cursor has no `path_prefix`,
    you can switch to any `path_prefix`. If your cursor has a `path_prefix` of "/Photos", you can switch it
    to "/Photos/Vacaction".

    When `include_media_info` is specified, files will only appear in delta responses when the media info is
    ready. If you use the `include_media_info` parameter, you must continue to pass the same value on subsequent
    calls using the returned cursor.

    **Important:** Unfortunately it is not possible to model correct Dropbox response with Swagger specification,
    due to [nested array](https://github.com/swagger-api/swagger-spec/issues/40) usage in delta response.

    Successful result [will return](https://gist.github.com/ando-takahiro/5203137) an array of delta `entries`.
    Each delta entry is a 2-item list of one of the following forms:

      * `[, ]` - Indicates that there is a file/folder at the given path. You should add the entry
      to your local state. The metadata value is the same as what would be returned by the `/metadata` call, except
      folder metadata doesn't have `hash` or `contents` fields. To correctly process delta entries:
        * If the new entry includes parent folders that don't yet exist in your local state, create those parent
        folders in your local state.
        * If the new entry is a file, replace whatever your local state has at path with the new entry.
        * If the new entry is a folder, check what your local state has at ``. If it's a file, replace it
        with the new entry. If it's a folder, apply the new `` to the folder, but don't modify the
        folder's children. If your local state doesn't yet include this path, create it as a folder.
        * If the new entry is a folder with the `read-only` field set to `true`, apply the read-only permission
        recursively to all files within the shared folder.
      * `[, null]` - Indicates that there is no file/folder at the given path. To update your local state
      to match, anything at path and all its children should be deleted. Deleting a folder in your Dropbox will
      sometimes send down a single deleted entry for that folder, and sometimes separate entries for the folder
      and all child paths. If your local state doesn't have anything at path, ignore this entry.

    **Note:** Dropbox treats file names in a case-insensitive but case-preserving way. To facilitate this,
    the `` values above are lower-cased versions of the actual path. The last path component of the
    `` value will be case-preserved.
  image: https://avatars.githubusercontent.com/u/559357?v=3
  humanURL: https://www.dropbox.com
  baseURL: https://api.dropbox.com//1//delta
  tags: Storage,Documents,Delta
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/dropbox/master/_listings/dropbox/delta-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/dropbox/master/_listings/dropbox/delta-post-openapi.md
- name: Dropbox Core A way to quickly get a cursor for the server's state, for use
    with /delta.
  x-api-slug: dropbox-core
  description: |-
    A way to quickly get a cursor for the server's state, for use with `/delta`.

    Unlike `/delta`, `/delta/latest_cursor` does not return any entries, so your app will not know about any
    existing files or folders in the Dropbox account. For example, if your app processes future delta entries
    and sees that a folder was deleted, your app won't know what files were in that folder. Use this endpoint
    if your app only needs to know about new files and modifications and doesn't need to know about files that
    already exist in Dropbox.

    If you need to build local state to match the server state in Dropbox, you should instead use `/delta`.
  image: https://avatars.githubusercontent.com/u/559357?v=3
  humanURL: https://www.dropbox.com
  baseURL: https://api.dropbox.com//1//delta/latest_cursor
  tags: Storage,Documents,Delta,Latest_cursor
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/dropbox/master/_listings/dropbox/deltalatest-cursor-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/dropbox/master/_listings/dropbox/deltalatest-cursor-post-openapi.md
- name: Dropbox Core Obtains metadata for all available revisions of a file, including
    the current revision.
  x-api-slug: dropbox-core
  description: |-
    Obtains metadata for all available revisions of a file, including the current revision.

    Only revisions up to thirty days old are available (or more if the Dropbox user has
    [Extended Version History](https://www.dropbox.com/help/113)). You can use the revision number in conjunction
    with the `/restore` call to revert the file to its previous state.
  image: https://avatars.githubusercontent.com/u/559357?v=3
  humanURL: https://www.dropbox.com
  baseURL: https://api.dropbox.com//1//revisions/{root}/{path}
  tags: Storage,Documents,Revisions,Root,Path
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/dropbox/master/_listings/dropbox/revisionsrootpath-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/dropbox/master/_listings/dropbox/revisionsrootpath-get-openapi.md
- name: Dropbox Core Restores a file path to a previous revision.
  x-api-slug: dropbox-core
  description: |-
    Restores a file path to a previous revision.

    Unlike downloading a file at a given revision and then re-uploading it, this call is atomic. It also saves
    a bunch of bandwidth.
  image: https://avatars.githubusercontent.com/u/559357?v=3
  humanURL: https://www.dropbox.com
  baseURL: https://api.dropbox.com//1//restore/{root}/{path}
  tags: Storage,Documents,Restore,Root,Path
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/dropbox/master/_listings/dropbox/restorerootpath-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/dropbox/master/_listings/dropbox/restorerootpath-post-openapi.md
- name: Dropbox Core Search for files and folders by name.
  x-api-slug: dropbox-core
  description: |-
    Returns metadata for all files and folders whose filename contains the given search string as a substring.

    Searches are limited to the folder path and its sub-folder hierarchy provided in the call.

    **Note:** Recent changes may not immediately be reflected in search results due to a short delay in indexing.
  image: https://avatars.githubusercontent.com/u/559357?v=3
  humanURL: https://www.dropbox.com
  baseURL: https://api.dropbox.com//1//search/{root}/{path}
  tags: Storage,Documents,Search,Root,Path
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/dropbox/master/_listings/dropbox/searchrootpath-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/dropbox/master/_listings/dropbox/searchrootpath-get-openapi.md
- name: Dropbox Core Search for files and folders by name.
  x-api-slug: dropbox-core
  description: |-
    Returns metadata for all files and folders whose filename contains the given search string as a substring.

    Searches are limited to the folder path and its sub-folder hierarchy provided in the call.

    **Note:** Recent changes may not immediately be reflected in search results due to a short delay in indexing.
  image: https://avatars.githubusercontent.com/u/559357?v=3
  humanURL: https://www.dropbox.com
  baseURL: https://api.dropbox.com//1//search/{root}/{path}
  tags: Storage,Documents,Search,Root,Path
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/dropbox/master/_listings/dropbox/searchrootpath-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/dropbox/master/_listings/dropbox/searchrootpath-post-openapi.md
- name: Dropbox Core Creates and returns a shared link to a file or folder.
  x-api-slug: dropbox-core
  description: |-
    Creates and returns a [shared link](https://www.dropbox.com/help/167) to a file or folder.

    Dropbox for Business users can set restrictions on shared links; the `visibility` field indicates what
    (if any) restrictions are set on this particular link. Possible values include:
      * `PUBLIC` - anyone can view
      * `TEAM_ONLY` - only the owner's team can view
      * `PASSWORD` - a password is required
      * `TEAM_AND_PASSWORD` - a combination of `TEAM_ONLY` and `PASSWORD` restrictions
      * `SHARED_FOLDER_ONLY` - only [members](https://www.dropbox.com/help/6636) of the enclosing shared folder can view

    Note that other values may be added at any time.
  image: https://avatars.githubusercontent.com/u/559357?v=3
  humanURL: https://www.dropbox.com
  baseURL: https://api.dropbox.com//1//shares/{root}/{path}
  tags: Storage,Documents,Shares,Root,Path
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/dropbox/master/_listings/dropbox/sharesrootpath-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/dropbox/master/_listings/dropbox/sharesrootpath-post-openapi.md
- name: Dropbox Core Returns a link directly to a file.
  x-api-slug: dropbox-core
  description: |-
    Returns a link directly to a file.

    Similar to [/shares](https://www.dropbox.com/developers/core/docs#shares). The difference is that this
    bypasses the Dropbox webserver, used to provide a preview of the file, so that you can effectively stream
    the contents of your media. This URL should not be used to display content directly in the browser.

    The `/media` link expires after four hours, allotting enough time to stream files, but not enough to leave
    a connection open indefinitely.
  image: https://avatars.githubusercontent.com/u/559357?v=3
  humanURL: https://www.dropbox.com
  baseURL: https://api.dropbox.com//1//media/{root}/{path}
  tags: Storage,Documents,Media,Root,Path
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/dropbox/master/_listings/dropbox/mediarootpath-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/dropbox/master/_listings/dropbox/mediarootpath-post-openapi.md
- name: Dropbox Core Creates and returns a copy_ref to a file.
  x-api-slug: dropbox-core
  description: |-
    Creates and returns a `copy_ref` to a file.

    This reference string can be used to copy that file to another user's Dropbox by passing it in as the
    `from_copy_ref` parameter on [/fileops/copy](https://www.dropbox.com/developers/core/docs#fileops-copy).
  image: https://avatars.githubusercontent.com/u/559357?v=3
  humanURL: https://www.dropbox.com
  baseURL: https://api.dropbox.com//1//copy_ref/{root}/{path}
  tags: Storage,Documents,Copy,Root,Path
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/dropbox/master/_listings/dropbox/copy-refrootpath-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/dropbox/master/_listings/dropbox/copy-refrootpath-get-openapi.md
- name: Dropbox Core Returns a list of all shared folders.
  x-api-slug: dropbox-core
  description: |-
    Returns a list of all shared folders the authenticated user has access to.

    This API call requires Full Dropbox or File type [permissions](https://www.dropbox.com/developers/reference/devguide#app-permissions).

    Note that `same_team` is only present if the linked account is a member of a Dropbox for Business team,
    and `member_id` is only present when this endpoint is called by a Dropbox for Business app and the user
    is on that team.

    The `membership` field only contains users who have joined the shared folder and does not include users who
    have been invited but have not accepted. When the `active` field is `false`, it means that a user has left
    a shared folder (but may still rejoin).
  image: https://avatars.githubusercontent.com/u/559357?v=3
  humanURL: https://www.dropbox.com
  baseURL: https://api.dropbox.com//1//shared_folders
  tags: Storage,Documents,Shared_folders
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/dropbox/master/_listings/dropbox/shared-folders-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/dropbox/master/_listings/dropbox/shared-folders-get-openapi.md
- name: Dropbox Core Returns metadata about a specific shared folder.
  x-api-slug: dropbox-core
  description: |-
    Returns metadata about a specific shared folder.

    This API call requires Full Dropbox or File type [permissions](https://www.dropbox.com/developers/reference/devguide#app-permissions).

    Note that `same_team` is only present if the linked account is a member of a Dropbox for Business team,
    and `member_id` is only present when this endpoint is called by a Dropbox for Business app and the user
    is on that team.

    The `membership` field only contains users who have joined the shared folder and does not include users who
    have been invited but have not accepted. When the `active` field is `false`, it means that a user has left
    a shared folder (but may still rejoin).
  image: https://avatars.githubusercontent.com/u/559357?v=3
  humanURL: https://www.dropbox.com
  baseURL: https://api.dropbox.com//1//shared_folders/{shared_folder_id}
  tags: Storage,Documents,Shared_folders,Shared_folder_id
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/dropbox/master/_listings/dropbox/shared-foldersshared-folder-id-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/dropbox/master/_listings/dropbox/shared-foldersshared-folder-id-get-openapi.md
- name: Dropbox Core Save a file from the specified URL into Dropbox.
  x-api-slug: dropbox-core
  description: |-
    Save a file from the specified URL into Dropbox.

    If the given path already exists, the file will be renamed to avoid the conflict (e.g. `myfile (1).txt`).
  image: https://avatars.githubusercontent.com/u/559357?v=3
  humanURL: https://www.dropbox.com
  baseURL: https://api.dropbox.com//1//save_url/{root}/{path}
  tags: Storage,Documents,URL,Root,Path
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/dropbox/master/_listings/dropbox/save-urlrootpath-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/dropbox/master/_listings/dropbox/save-urlrootpath-post-openapi.md
- name: Dropbox Core Check the status of a save URL job.
  x-api-slug: dropbox-core
  description: "Check the status of a [save URL](https://www.dropbox.com/developers/core/docs#save-url)
    job.\n\nStatus field may have one of the following values:\n  * `PENDING` \u2013
    The job has not yet started.\n  * `DOWNLOADING` \u2013 The job has started but
    hasn't yet completed.\n  * `COMPLETE` \u2013 The job is complete.\n  * `FAILED`
    \u2013 The job failed. An additional `error` field will describe the failure."
  image: https://avatars.githubusercontent.com/u/559357?v=3
  humanURL: https://www.dropbox.com
  baseURL: https://api.dropbox.com//1//save_url_job/{job-id}
  tags: Storage,Documents,Save_url_job,Job-id
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/dropbox/master/_listings/dropbox/save-url-jobjobid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/dropbox/master/_listings/dropbox/save-url-jobjobid-get-openapi.md
- name: Dropbox Core Copies a file or folder to a new location.
  x-api-slug: dropbox-core
  description: Copies a file or folder to a new location.
  image: https://avatars.githubusercontent.com/u/559357?v=3
  humanURL: https://www.dropbox.com
  baseURL: https://api.dropbox.com//1//fileops/copy
  tags: Storage,Documents,Fileops,Copy
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/dropbox/master/_listings/dropbox/fileopscopy-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/dropbox/master/_listings/dropbox/fileopscopy-post-openapi.md
- name: Dropbox Core Creates a folder.
  x-api-slug: dropbox-core
  description: Creates a folder.
  image: https://avatars.githubusercontent.com/u/559357?v=3
  humanURL: https://www.dropbox.com
  baseURL: https://api.dropbox.com//1//fileops/create_folder
  tags: Storage,Documents,Fileops,Create_folder
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/dropbox/master/_listings/dropbox/fileopscreate-folder-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/dropbox/master/_listings/dropbox/fileopscreate-folder-post-openapi.md
- name: Dropbox Core Deletes a file or folder.
  x-api-slug: dropbox-core
  description: Deletes a file or folder.
  image: https://avatars.githubusercontent.com/u/559357?v=3
  humanURL: https://www.dropbox.com
  baseURL: https://api.dropbox.com//1//fileops/delete
  tags: Storage,Documents,Fileops,Delete
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/dropbox/master/_listings/dropbox/fileopsdelete-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/dropbox/master/_listings/dropbox/fileopsdelete-post-openapi.md
- name: Dropbox Core Moves a file or folder to a new location.
  x-api-slug: dropbox-core
  description: Moves a file or folder to a new location.
  image: https://avatars.githubusercontent.com/u/559357?v=3
  humanURL: https://www.dropbox.com
  baseURL: https://api.dropbox.com//1//fileops/move
  tags: Storage,Documents,Fileops,Move
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/dropbox/master/_listings/dropbox/fileopsmove-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/dropbox/master/_listings/dropbox/fileopsmove-post-openapi.md
- name: Dropbox Core
  x-api-slug: dropbox-core
  description: Dropbox is a file hosting service operated by Dropbox, Inc., that offers
    cloud storage, file synchronization, and client software. Dropbox allows users
    to create a special folder on each of their computers, which Dropbox then synchronizes
    so that it appears to be the same folder (with the same contents) regardless of
    which computer is used to view it. Files placed in this folder also are accessible
    through a website and mobile phone applications.
  image: https://avatars.githubusercontent.com/u/559357?v=3
  humanURL: https://www.dropbox.com
  baseURL: https://api.dropbox.com//1
  tags: Dropbox
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/dropbox/master/_listings/dropbox/openapi.md
- name: Dropbox Notify A long-poll endpoint to wait for changes on an account.
  x-api-slug: dropbox-notify
  description: |-
    A long-poll endpoint to wait for changes on an account. In conjunction with [/delta](https://www.dropbox.com/developers/core/docs#delta),
    this call gives you a low-latency way to monitor an account for file changes.

    Note that this call goes to **api-notify.dropbox.com** instead of *api.dropbox.com*.

    Unlike most other API endpoints, this call does not require OAuth authentication. The passed in `cursor` can
    only be acquired via an authenticated call to [/delta](https://www.dropbox.com/developers/core/docs#delta).
  image: https://avatars.githubusercontent.com/u/559357?v=3
  humanURL: https://www.dropbox.com
  baseURL: https://api-notify.dropbox.com//1//longpoll_delta
  tags: Documents, Notify
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/dropbox/master/_listings/dropbox/longpoll-delta-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/dropbox/master/_listings/dropbox/longpoll-delta-get-openapi.md
- name: Dropbox Notify
  x-api-slug: dropbox-notify
  description: Dropbox is a file hosting service operated by Dropbox, Inc., that offers
    cloud storage, file synchronization, and client software. Dropbox allows users
    to create a special folder on each of their computers, which Dropbox then synchronizes
    so that it appears to be the same folder (with the same contents) regardless of
    which computer is used to view it. Files placed in this folder also are accessible
    through a website and mobile phone applications.
  image: https://avatars.githubusercontent.com/u/559357?v=3
  humanURL: https://www.dropbox.com
  baseURL: https://api-notify.dropbox.com//1
  tags: Dropbox
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/dropbox/master/_listings/dropbox/openapi.md
x-common:
- type: x-application-management
  url: https://www.dropbox.com/developers/apps
- type: x-base
  url: https://api.dropbox.com/
- type: x-blog
  url: https://blog.dropbox.com/
- type: x-blog-rss
  url: https://blog.dropbox.com/feed/
- type: x-branding
  url: https://www.dropbox.com/developers/reference/branding
- type: x-branding
  url: https://www.dropbox.com/branding
- type: x-contact-form
  url: https://www.dropbox.com/developers/contact
- type: x-crunchbase
  url: http://www.crunchbase.com/company/dropbox
- type: x-developer
  url: https://www.dropbox.com/developers
- type: x-faq
  url: https://www.dropbox.com/developers/support
- type: x-forum
  url: https://www.dropboxforum.com/hc/communities/public/topics/200209245-API-Development
- type: x-github
  url: https://github.com/dropbox
- type: x-pricing
  url: https://www.dropbox.com/plans
- type: x-privacy
  url: https://www.dropbox.com/privacy
- type: x-stack-overflow
  url: http://stackoverflow.com/questions/tagged/dropbox-api?sort=votes&pagesize=15
- type: x-support
  url: https://www.dropbox.com/help
- type: x-terms-of-service
  url: https://www.dropbox.com/privacy#terms
- type: x-transparency-report
  url: https://www.dropbox.com/transparency
- type: x-twitter
  url: https://twitter.com/dropbox
- type: x-webhooks
  url: https://www.dropbox.com/developers/webhooks/docs
- type: x-website
  url: https://www.dropbox.com
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---