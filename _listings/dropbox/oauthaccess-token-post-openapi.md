---
swagger: "2.0"
x-collection-name: Dropbox
x-complete: 0
info:
  title: Dropbox Datastore API OAuth Access Token
  description: /oauth/access_token
  version: "1"
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
      summary: Chunked Upload
      description: /chunked_upload
      operationId: chunked-upload
      x-api-path-slug: chunked-upload-put
      parameters:
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
  /disable_access_token:
    post:
      summary: Disable Access Token
      description: /disable_access_token
      operationId: disable-access-token
      x-api-path-slug: disable-access-token-post
      responses:
        200:
          description: OK
      tags:
      - Disable
      - Access
      - Token
  /account/info:
    get:
      summary: Retrieves information about the user's account.
      description: Retrieves information about the user's account.
      operationId: retrieves-information-about-the-users-account
      x-api-path-slug: accountinfo-get
      parameters:
      - in: query
        name: locale
        description: Use to specify language settings for user error messages and
          other language specific text
      responses:
        200:
          description: OK
      tags:
      - Storage
      - Documents
      - Account
      - Info
  /metadata/{root}/{path}:
    get:
      summary: Retrieves file and folder metadata.
      description: |-
        Retrieves file and folder metadata.

        **Note:** `modified`, `rev`, and `revision` aren't returned in the metadata for the root/top-level path.
      operationId: retrieves-file-and-folder-metadatanote-modified-rev-and-revision-arent-returned-in-the-metadata-for-
      x-api-path-slug: metadatarootpath-get
      parameters:
      - in: query
        name: file_limit
        description: Default is 10,000 (max is 25,000)
      - in: query
        name: hash
        description: Each call to `/metadata` on a folder will return a `hash` field,
          generated by hashing all of the metadatacontained in that response
      - in: query
        name: include_deleted
        description: Only applicable when `list` is set
      - in: query
        name: include_media_info
        description: If `true`, each file will include a `photo_info` dictionary for
          photos and a `video_info` dictionaryfor videos with additional media info
      - in: query
        name: include_membership
        description: If `true`, metadata for a shared folder will include a list of
          members and a list of groups
      - in: query
        name: list
        description: The strings `true` and `false` are valid values
      - in: query
        name: locale
        description: The metadata returned will have its `size` field translated based
          on the given `locale`
      - in: path
        name: path
        description: The path to the file or folder
      - in: query
        name: rev
        description: If you include a particular revision number, then only the metadata
          for that revision will be returned
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
      - Metadata
      - Root
      - Path
  /delta:
    post:
      summary: A way of letting you keep up with changes to files and folders in a
        user's Dropbox.
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
      operationId: a-way-of-letting-you-keep-up-with-changes-to-files-and-folders-in-a-users-dropboxyou-can-periodicall
      x-api-path-slug: delta-post
      parameters:
      - in: formData
        name: cursor
        description: A string that is used to keep track of your current state
      - in: formData
        name: include_media_info
        description: If `true`, each file will include a `photo_info` dictionary for
          photos and a `video_info` dictionary forvideos with additional media info
      - in: formData
        name: locale
        description: The metadata returned will have its `size` field translated based
          on the given `locale`
      - in: formData
        name: path_prefix
        description: If present, this parameter filters the response to only include
          entries at or under the specified path
      responses:
        200:
          description: OK
      tags:
      - Storage
      - Documents
      - Delta
  /delta/latest_cursor:
    post:
      summary: Latest Cursor
      description: /delta/latest_cursor
      operationId: deltalatest-cursor
      x-api-path-slug: deltalatest-cursor-post
      parameters:
      - in: query
        name: include_media_info
        description: If true, the returned cursor will be encoded with include_media_info
          set to true for use with /delta
      - in: query
        name: path_prefix
        description: If present, the returned cursor will be encoded with a path_prefix
          for the specified path for use with /delta
      responses:
        200:
          description: OK
      tags:
      - Delta
      - Latest
      - Cursor
  /revisions/{root}/{path}:
    get:
      summary: Obtains metadata for all available revisions of a file, including the
        current revision.
      description: |-
        Obtains metadata for all available revisions of a file, including the current revision.

        Only revisions up to thirty days old are available (or more if the Dropbox user has
        [Extended Version History](https://www.dropbox.com/help/113)). You can use the revision number in conjunction
        with the `/restore` call to revert the file to its previous state.
      operationId: obtains-metadata-for-all-available-revisions-of-a-file-including-the-current-revisiononly-revisions-
      x-api-path-slug: revisionsrootpath-get
      parameters:
      - in: query
        name: locale
        description: The metadata returned will have its `size` field translated based
          on the given `locale`
      - in: path
        name: path
        description: The path to the file
      - in: query
        name: rev_limit
        description: Default is 10
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
      - Revisions
      - Root
      - Path
  /restore/{root}/{path}:
    post:
      summary: Restores a file path to a previous revision.
      description: |-
        Restores a file path to a previous revision.

        Unlike downloading a file at a given revision and then re-uploading it, this call is atomic. It also saves
        a bunch of bandwidth.
      operationId: restores-a-file-path-to-a-previous-revisionunlike-downloading-a-file-at-a-given-revision-and-then-re
      x-api-path-slug: restorerootpath-post
      parameters:
      - in: formData
        name: locale
        description: The metadata returned will have its `size` field translated based
          on the given `locale`
      - in: path
        name: path
        description: The path to the file
      - in: formData
        name: rev
        description: The revision of the file to restore
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
      - Restore
      - Root
      - Path
  /search/{root}/{path}:
    get:
      summary: Search for files and folders by name.
      description: |-
        Returns metadata for all files and folders whose filename contains the given search string as a substring.

        Searches are limited to the folder path and its sub-folder hierarchy provided in the call.

        **Note:** Recent changes may not immediately be reflected in search results due to a short delay in indexing.
      operationId: returns-metadata-for-all-files-and-folders-whose-filename-contains-the-given-search-string-as-a-subs
      x-api-path-slug: searchrootpath-get
      parameters:
      - in: query
        name: file_limit
        description: The maximum and default value is 1,000
      - in: query
        name: include_deleted
        description: If this parameter is set to `true`, then files and folders that
          have been deleted will also be includedin the search
      - in: query
        name: include_membership
        description: If `true`, metadata for a shared folder will include a list of
          members and a list of groups
      - in: query
        name: locale
        description: The metadata returned will have its `size` field translated based
          on the given `locale`
      - in: path
        name: path
        description: The path to the folder you want to search from
      - in: query
        name: query
        description: The search string
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
      - Search
      - Root
      - Path
    post:
      summary: Search for files and folders by name.
      description: |-
        Returns metadata for all files and folders whose filename contains the given search string as a substring.

        Searches are limited to the folder path and its sub-folder hierarchy provided in the call.

        **Note:** Recent changes may not immediately be reflected in search results due to a short delay in indexing.
      operationId: returns-metadata-for-all-files-and-folders-whose-filename-contains-the-given-search-string-as-a-subs
      x-api-path-slug: searchrootpath-post
      parameters:
      - in: formData
        name: file_limit
        description: The maximum and default value is 1,000
      - in: formData
        name: include_deleted
        description: If this parameter is set to `true`, then files and folders that
          have been deleted will also be includedin the search
      - in: formData
        name: include_membership
        description: If `true`, metadata for a shared folder will include a list of
          members and a list of groups
      - in: formData
        name: locale
        description: The metadata returned will have its `size` field translated based
          on the given `locale`
      - in: path
        name: path
        description: The path to the folder you want to search from
      - in: formData
        name: query
        description: The search string
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
      - Search
      - Root
      - Path
  /shares/{root}/{path}:
    post:
      summary: Creates and returns a shared link to a file or folder.
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
      operationId: creates-and-returns-a-shared-linkhttpswwwdropboxcomhelp167-to-a-file-or-folderdropbox-for-business-u
      x-api-path-slug: sharesrootpath-post
      parameters:
      - in: formData
        name: locale
        description: Use to specify language settings for user error messages and
          other language specific text
      - in: path
        name: path
        description: The path to the file or folder you want to link to
      - in: path
        name: root
        description: 'Root folder: `auto` - automatically determines the appropriate
          root folder using your apps permissionlevel (recommended); `sandbox` - the
          codename for app folder level; `dropbox` - full dropbox access'
      - in: formData
        name: short_url
        description: When `true` (default), the URL returned will be shortened using
          the Dropbox URL shortener
      responses:
        200:
          description: OK
      tags:
      - Storage
      - Documents
      - Shares
      - Root
      - Path
  /media/{root}/{path}:
    post:
      summary: Returns a link directly to a file.
      description: |-
        Returns a link directly to a file.

        Similar to [/shares](https://www.dropbox.com/developers/core/docs#shares). The difference is that this
        bypasses the Dropbox webserver, used to provide a preview of the file, so that you can effectively stream
        the contents of your media. This URL should not be used to display content directly in the browser.

        The `/media` link expires after four hours, allotting enough time to stream files, but not enough to leave
        a connection open indefinitely.
      operationId: returns-a-link-directly-to-a-filesimilar-to-shareshttpswwwdropboxcomdeveloperscoredocsshares-the-dif
      x-api-path-slug: mediarootpath-post
      parameters:
      - in: formData
        name: locale
        description: Use to specify language settings for user error messages and
          other language specific text
      - in: path
        name: path
        description: The path to the media file you want a direct link to
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
      - Media
      - Root
      - Path
  /copy_ref/{root}/{path}:
    get:
      summary: Creates and returns a copy_ref to a file.
      description: |-
        Creates and returns a `copy_ref` to a file.

        This reference string can be used to copy that file to another user's Dropbox by passing it in as the
        `from_copy_ref` parameter on [/fileops/copy](https://www.dropbox.com/developers/core/docs#fileops-copy).
      operationId: creates-and-returns-a-copy-ref-to-a-filethis-reference-string-can-be-used-to-copy-that-file-to-anoth
      x-api-path-slug: copy-refrootpath-get
      parameters:
      - in: path
        name: path
        description: The path to the file you want a `copy_ref` to refer to
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
      - Copy
      - Root
      - Path
  /shared_folders:
    get:
      summary: Returns a list of all shared folders.
      description: |-
        Returns a list of all shared folders the authenticated user has access to.

        This API call requires Full Dropbox or File type [permissions](https://www.dropbox.com/developers/reference/devguide#app-permissions).

        Note that `same_team` is only present if the linked account is a member of a Dropbox for Business team,
        and `member_id` is only present when this endpoint is called by a Dropbox for Business app and the user
        is on that team.

        The `membership` field only contains users who have joined the shared folder and does not include users who
        have been invited but have not accepted. When the `active` field is `false`, it means that a user has left
        a shared folder (but may still rejoin).
      operationId: returns-a-list-of-all-shared-folders-the-authenticated-user-has-access-tothis-api-call-requires-full
      x-api-path-slug: shared-folders-get
      parameters:
      - in: query
        name: include_membership
        description: If `true`, include a list of members and a list of groups for
          the shared folder
      responses:
        200:
          description: OK
      tags:
      - Storage
      - Documents
      - Shared_folders
  /shared_folders/{shared_folder_id}:
    get:
      summary: Returns metadata about a specific shared folder.
      description: |-
        Returns metadata about a specific shared folder.

        This API call requires Full Dropbox or File type [permissions](https://www.dropbox.com/developers/reference/devguide#app-permissions).

        Note that `same_team` is only present if the linked account is a member of a Dropbox for Business team,
        and `member_id` is only present when this endpoint is called by a Dropbox for Business app and the user
        is on that team.

        The `membership` field only contains users who have joined the shared folder and does not include users who
        have been invited but have not accepted. When the `active` field is `false`, it means that a user has left
        a shared folder (but may still rejoin).
      operationId: returns-metadata-about-a-specific-shared-folderthis-api-call-requires-full-dropbox-or-file-type-perm
      x-api-path-slug: shared-foldersshared-folder-id-get
      parameters:
      - in: query
        name: include_membership
        description: If `true`, include a list of members and a list of groups for
          the shared folder
      - in: path
        name: shared_folder_id
        description: The ID of a specific shared folder
      responses:
        200:
          description: OK
      tags:
      - Storage
      - Documents
      - Shared_folders
      - Shared_folder_id
  /save_url/{root}/{path}:
    post:
      summary: Save a file from the specified URL into Dropbox.
      description: |-
        Save a file from the specified URL into Dropbox.

        If the given path already exists, the file will be renamed to avoid the conflict (e.g. `myfile (1).txt`).
      operationId: save-a-file-from-the-specified-url-into-dropboxif-the-given-path-already-exists-the-file-will-be-ren
      x-api-path-slug: save-urlrootpath-post
      parameters:
      - in: path
        name: path
        description: The path in Dropbox where the file will be saved
      - in: path
        name: root
        description: 'Root folder: `auto` - automatically determines the appropriate
          root folder using your apps permissionlevel (recommended); `sandbox` - the
          codename for app folder level; `dropbox` - full dropbox access'
      - in: formData
        name: url
        description: The URL to be fetched
      responses:
        200:
          description: OK
      tags:
      - Storage
      - Documents
      - URL
      - Root
      - Path
  /save_url_job/{job-id}:
    get:
      summary: Check the status of a save URL job.
      description: |-
        Check the status of a [save URL](https://www.dropbox.com/developers/core/docs#save-url) job.

        Status field may have one of the following values:
          * `PENDING` ??? The job has not yet started.
          * `DOWNLOADING` ??? The job has started but hasn't yet completed.
          * `COMPLETE` ??? The job is complete.
          * `FAILED` ??? The job failed. An additional `error` field will describe the failure.
      operationId: check-the-status-of-a-save-urlhttpswwwdropboxcomdeveloperscoredocssaveurl-jobstatus-field-may-have-o
      x-api-path-slug: save-url-jobjobid-get
      parameters:
      - in: path
        name: job-id
        description: A job ID returned from [/save_url](https://www
      responses:
        200:
          description: OK
      tags:
      - Storage
      - Documents
      - Save_url_job
      - Job-id
  /fileops/copy:
    post:
      summary: Copies a file or folder to a new location.
      description: Copies a file or folder to a new location.
      operationId: copies-a-file-or-folder-to-a-new-location
      x-api-path-slug: fileopscopy-post
      parameters:
      - in: formData
        name: from_copy_ref
        description: Specifies a `copy_ref` generated from a previous [/copy_ref](https://www
      - in: formData
        name: from_path
        description: Specifies the file or folder to be copied from relative to `root`
      - in: formData
        name: locale
        description: The metadata returned will have its `size` field translated based
          on the given locale
      - in: formData
        name: root
        description: The root relative to which `from_path` and `to_path` are specified
      - in: formData
        name: to_path
        description: Specifies the destination path, *including the new name for the
          file or folder*, relative to `root`
      responses:
        200:
          description: OK
      tags:
      - Storage
      - Documents
      - Fileops
      - Copy
  /fileops/create_folder:
    post:
      summary: Create Folder
      description: /fileops/create_folder
      operationId: fileopscreate-folder
      x-api-path-slug: fileopscreate-folder-post
      parameters:
      - in: query
        name: locale
        description: The metadata returned will have its size field translated based
          on the given locale
      - in: query
        name: path
        description: The path to the new folder to create relative to root
      - in: query
        name: root
        description: The root relative to which path is specified
      responses:
        200:
          description: OK
      tags:
      - Fileops
      - Create
      - Folder
  /fileops/delete:
    post:
      summary: Deletes a file or folder.
      description: Deletes a file or folder.
      operationId: deletes-a-file-or-folder
      x-api-path-slug: fileopsdelete-post
      parameters:
      - in: formData
        name: locale
        description: The metadata returned will have its `size` field translated based
          on the given locale
      - in: formData
        name: path
        description: The path to the file or folder to be deleted
      - in: formData
        name: root
        description: The root relative to which `path` is specified
      responses:
        200:
          description: OK
      tags:
      - Storage
      - Documents
      - Fileops
      - Delete
  /fileops/move:
    post:
      summary: Moves a file or folder to a new location.
      description: Moves a file or folder to a new location.
      operationId: moves-a-file-or-folder-to-a-new-location
      x-api-path-slug: fileopsmove-post
      parameters:
      - in: formData
        name: from_path
        description: Specifies the file or folder to be moved from relative to `root`
      - in: formData
        name: locale
        description: The metadata returned will have its `size` field translated based
          on the given locale
      - in: formData
        name: root
        description: The root relative to which `from_path` and `to_path` are specified
      - in: formData
        name: to_path
        description: Specifies the destination path, *including the new name for the
          file or folder*, relative to `root`
      responses:
        200:
          description: OK
      tags:
      - Storage
      - Documents
      - Fileops
      - Move
  /files:
    get:
      summary: Get File
      description: /files (GET)
      operationId: files-get
      x-api-path-slug: files-get
      parameters:
      - in: query
        name: path
        description: The path to the file you want to retrieve
      - in: query
        name: rev
        description: The revision of the file to retrieve
      responses:
        200:
          description: OK
      tags:
      - Files
  /media:
    post:
      summary: Add Media
      description: /media
      operationId: media
      x-api-path-slug: media-post
      parameters:
      - in: query
        name: locale
        description: Use to specify language settings for user error messages and
          other language specific text
      responses:
        200:
          description: OK
      tags:
      - Media
  /metadata:
    get:
      summary: Get Meta Data
      description: /metadata
      operationId: metadata
      x-api-path-slug: metadata-get
      parameters:
      - in: query
        name: file_limit
        description: Default is 10,000 (max is 25,000)
      - in: query
        name: hash
        description: Each call to /metadata on a folder will return a hash field,
          generated by hashing all of the metadata contained in that response
      - in: query
        name: include_deleted
        description: Only applicable when list is set
      - in: query
        name: include_media_info
        description: If true, each file will include a photo_info dictionary for photos
          and a video_info dictionary for videos with additional media info
      - in: query
        name: include_membership
        description: If true, metadata for a shared folder will include a list of
          the members of the shared folder
      - in: query
        name: list
        description: The strings true and false are valid values
      - in: query
        name: locale
        description: The metadata returned will have its size field translated based
          on the given locale
      - in: query
        name: rev
        description: If you include a particular revision number, then only the metadata
          for that revision will be returned
      responses:
        200:
          description: OK
      tags:
      - Metadata
  /oauth/access_token:
    post:
      summary: OAuth Access Token
      description: /oauth/access_token
      operationId: oauthaccess-token
      x-api-path-slug: oauthaccess-token-post
      responses:
        200:
          description: OK
      tags:
      - Oauth
      - Access
      - Token
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