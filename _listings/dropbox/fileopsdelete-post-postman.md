{
  "info": {
    "name": "Dropbox Core Deletes a file or folder.",
    "_postman_id": "40de1790-f789-4834-8f28-9f35b323bbbe",
    "description": "Deletes a file or folder.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Storage",
      "item": [
        {
          "id": "dd81dd82-5950-4e39-b909-d218b8f8123e",
          "name": "this-endpoint-should-be-used-by-apps-transitioning-from-oauth-1-to-oauth-2-it-will-return-an-oauth-2",
          "request": {
            "url": "http://api.dropbox.com/1/oauth2/token_from_oauth1",
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "This endpoint should be used by apps transitioning from OAuth 1 to OAuth 2. It will return an OAuth 2 token\nfor the authenticated user."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "06458523-b066-4379-bcd0-26c3a57ec0bf"
            }
          ]
        },
        {
          "id": "5c3ecbc6-c76f-4485-a08a-27bf17029b4e",
          "name": "disables-the-access-token-used-to-authenticate-the-call-this-method-works-for-oauth-1-and-oauth-2-to",
          "request": {
            "url": "http://api.dropbox.com/1/disable_access_token",
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "Disables the access token used to authenticate the call. This method works for OAuth 1 and OAuth 2 tokens."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "61dfdf75-bd5a-4ebd-bb23-cd87762c0e1e"
            }
          ]
        },
        {
          "id": "eb489a65-018b-495f-bf97-6e1d94952bae",
          "name": "retrieves-information-about-the-users-account",
          "request": {
            "url": "http://api.dropbox.com/1/account/info?locale=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Retrieves information about the user's account."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "0d88f212-987b-4b86-b1ad-65ba4e47e3af"
            }
          ]
        },
        {
          "id": "d9a02efb-cc6c-4262-9c1d-0e8e789d1237",
          "name": "retrieves-file-and-folder-metadatanote-modified-rev-and-revision-arent-returned-in-the-metadata-for-",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.dropbox.com",
              "path": [
                "1",
                "metadata/:root/:path"
              ],
              "query": [
                {
                  "key": "file_limit",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "hash",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "include_deleted",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "include_media_info",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "include_membership",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "list",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "locale",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "rev",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "path",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "root",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Retrieves file and folder metadata.\n\n**Note:** `modified`, `rev`, and `revision` aren't returned in the metadata for the root/top-level path."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c3c1e102-1701-47d0-baca-c2b70da04247"
            }
          ]
        },
        {
          "id": "5acf19e3-d0b7-443c-9baa-d45175a9361e",
          "name": "a-way-of-letting-you-keep-up-with-changes-to-files-and-folders-in-a-users-dropboxyou-can-periodicall",
          "request": {
            "url": "http://api.dropbox.com/1/delta",
            "method": "POST",
            "body": {
              "mode": "urlencoded",
              "urlencoded": [
                {
                  "key": "cursor",
                  "value": "{}",
                  "disabled": false,
                  "description": "A string that is used to keep track of your current state"
                },
                {
                  "key": "include_media_info",
                  "value": "{}",
                  "disabled": false,
                  "description": "If `true`, each file will include a `photo_info` dictionary for photos and a `video_info` dictionary forvideos with additional media info"
                },
                {
                  "key": "locale",
                  "value": "{}",
                  "disabled": false,
                  "description": "The metadata returned will have its `size` field translated based on the given `locale`"
                },
                {
                  "key": "path_prefix",
                  "value": "{}",
                  "disabled": false,
                  "description": "If present, this parameter filters the response to only include entries at or under the specified path"
                }
              ]
            },
            "description": "A way of letting you keep up with changes to files and folders in a user's Dropbox.\n\nYou can periodically call `/delta` to get a list of \"delta entries\", which are instructions on how to\nupdate your local state to match the server's state.\n\nIf you use the `path_prefix` parameter, you must continue to pass the correct prefix on subsequent calls\nusing the returned cursor. You can switch the `path_prefix` on any existing cursor to a descendant of the\nexisting `path_prefix` on subsequent calls to `/delta`. For example if your cursor has no `path_prefix`,\nyou can switch to any `path_prefix`. If your cursor has a `path_prefix` of \"/Photos\", you can switch it\nto \"/Photos/Vacaction\".\n\nWhen `include_media_info` is specified, files will only appear in delta responses when the media info is\nready. If you use the `include_media_info` parameter, you must continue to pass the same value on subsequent\ncalls using the returned cursor.\n\n**Important:** Unfortunately it is not possible to model correct Dropbox response with Swagger specification,\ndue to [nested array](https://github.com/swagger-api/swagger-spec/issues/40) usage in delta response.\n\nSuccessful result [will return](https://gist.github.com/ando-takahiro/5203137) an array of delta `entries`.\nEach delta entry is a 2-item list of one of the following forms:\n\n  * `[, ]` - Indicates that there is a file/folder at the given path. You should add the entry\n  to your local state. The metadata value is the same as what would be returned by the `/metadata` call, except\n  folder metadata doesn't have `hash` or `contents` fields. To correctly process delta entries:\n    * If the new entry includes parent folders that don't yet exist in your local state, create those parent\n    folders in your local state.\n    * If the new entry is a file, replace whatever your local state has at path with the new entry.\n    * If the new entry is a folder, check what your local state has at ``. If it's a file, replace it\n    with the new entry. If it's a folder, apply the new `` to the folder, but don't modify the\n    folder's children. If your local state doesn't yet include this path, create it as a folder.\n    * If the new entry is a folder with the `read-only` field set to `true`, apply the read-only permission\n    recursively to all files within the shared folder.\n  * `[, null]` - Indicates that there is no file/folder at the given path. To update your local state\n  to match, anything at path and all its children should be deleted. Deleting a folder in your Dropbox will\n  sometimes send down a single deleted entry for that folder, and sometimes separate entries for the folder\n  and all child paths. If your local state doesn't have anything at path, ignore this entry.\n\n**Note:** Dropbox treats file names in a case-insensitive but case-preserving way. To facilitate this,\nthe `` values above are lower-cased versions of the actual path. The last path component of the\n`` value will be case-preserved."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e85d2f67-bd20-4524-9403-bdca3970047f"
            }
          ]
        },
        {
          "id": "f8670f03-221d-41bc-8ae0-741cb6afcb8b",
          "name": "a-way-to-quickly-get-a-cursor-for-the-servers-state-for-use-with-deltaunlike-delta-deltalatest-curso",
          "request": {
            "url": "http://api.dropbox.com/1/delta/latest_cursor",
            "method": "POST",
            "body": {
              "mode": "urlencoded",
              "urlencoded": [
                {
                  "key": "include_media_info",
                  "value": "{}",
                  "disabled": false,
                  "description": "If `true`, the returned cursor will be encoded with `include_media_info` set to `true` for usewith `/delta`"
                },
                {
                  "key": "path_prefix",
                  "value": "{}",
                  "disabled": false,
                  "description": "If present, the returned cursor will be encoded with a `path_prefix` for the specified path for usewith `/delta`"
                }
              ]
            },
            "description": "A way to quickly get a cursor for the server's state, for use with `/delta`.\n\nUnlike `/delta`, `/delta/latest_cursor` does not return any entries, so your app will not know about any\nexisting files or folders in the Dropbox account. For example, if your app processes future delta entries\nand sees that a folder was deleted, your app won't know what files were in that folder. Use this endpoint\nif your app only needs to know about new files and modifications and doesn't need to know about files that\nalready exist in Dropbox.\n\nIf you need to build local state to match the server state in Dropbox, you should instead use `/delta`."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "16739bfe-7b25-4a3d-b50c-aad567789f3a"
            }
          ]
        },
        {
          "id": "d08ae4aa-1ddd-4149-b6f3-5b07ef3ab9f2",
          "name": "obtains-metadata-for-all-available-revisions-of-a-file-including-the-current-revisiononly-revisions-",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.dropbox.com",
              "path": [
                "1",
                "revisions/:root/:path"
              ],
              "query": [
                {
                  "key": "locale",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "rev_limit",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "path",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "root",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Obtains metadata for all available revisions of a file, including the current revision.\n\nOnly revisions up to thirty days old are available (or more if the Dropbox user has\n[Extended Version History](https://www.dropbox.com/help/113)). You can use the revision number in conjunction\nwith the `/restore` call to revert the file to its previous state."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ebe307d7-ac6f-4167-9844-a5c6a22afb0a"
            }
          ]
        },
        {
          "id": "9c497ae7-ee6b-433f-b8b2-5dbc385ace6b",
          "name": "restores-a-file-path-to-a-previous-revisionunlike-downloading-a-file-at-a-given-revision-and-then-re",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.dropbox.com",
              "path": [
                "1",
                "restore/:root/:path"
              ],
              "variable": [
                {
                  "id": "path",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "root",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "POST",
            "body": {
              "mode": "urlencoded",
              "urlencoded": [
                {
                  "key": "locale",
                  "value": "{}",
                  "disabled": false,
                  "description": "The metadata returned will have its `size` field translated based on the given `locale`"
                },
                {
                  "key": "rev",
                  "value": "{}",
                  "disabled": false,
                  "description": "The revision of the file to restore"
                }
              ]
            },
            "description": "Restores a file path to a previous revision.\n\nUnlike downloading a file at a given revision and then re-uploading it, this call is atomic. It also saves\na bunch of bandwidth."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a2ef928e-30fd-4f78-a371-2533fda551bc"
            }
          ]
        },
        {
          "id": "64d0353c-30ab-4d5d-b764-a35e2a463156",
          "name": "returns-metadata-for-all-files-and-folders-whose-filename-contains-the-given-search-string-as-a-subs",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.dropbox.com",
              "path": [
                "1",
                "search/:root/:path"
              ],
              "query": [
                {
                  "key": "file_limit",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "include_deleted",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "include_membership",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "locale",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "query",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "path",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "root",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns metadata for all files and folders whose filename contains the given search string as a substring.\n\nSearches are limited to the folder path and its sub-folder hierarchy provided in the call.\n\n**Note:** Recent changes may not immediately be reflected in search results due to a short delay in indexing."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a4dfbc1f-b7da-4c48-9efa-d9abee38e8e9"
            }
          ]
        },
        {
          "id": "9f1256ff-6ada-4591-82d3-f6d063a16bb5",
          "name": "returns-metadata-for-all-files-and-folders-whose-filename-contains-the-given-search-string-as-a-subs",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.dropbox.com",
              "path": [
                "1",
                "search/:root/:path"
              ],
              "variable": [
                {
                  "id": "path",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "root",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "POST",
            "body": {
              "mode": "urlencoded",
              "urlencoded": [
                {
                  "key": "file_limit",
                  "value": "{}",
                  "disabled": false,
                  "description": "The maximum and default value is 1,000"
                },
                {
                  "key": "include_deleted",
                  "value": "{}",
                  "disabled": false,
                  "description": "If this parameter is set to `true`, then files and folders that have been deleted will also be includedin the search"
                },
                {
                  "key": "include_membership",
                  "value": "{}",
                  "disabled": false,
                  "description": "If `true`, metadata for a shared folder will include a list of members and a list of groups"
                },
                {
                  "key": "locale",
                  "value": "{}",
                  "disabled": false,
                  "description": "The metadata returned will have its `size` field translated based on the given `locale`"
                },
                {
                  "key": "query",
                  "value": "{}",
                  "disabled": false,
                  "description": "The search string"
                }
              ]
            },
            "description": "Returns metadata for all files and folders whose filename contains the given search string as a substring.\n\nSearches are limited to the folder path and its sub-folder hierarchy provided in the call.\n\n**Note:** Recent changes may not immediately be reflected in search results due to a short delay in indexing."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "dffc4e7c-3ffd-4987-a1f6-9e1052ca9d15"
            }
          ]
        },
        {
          "id": "03c90455-ece4-4421-8768-bdb47ecee80b",
          "name": "creates-and-returns-a-shared-linkhttpswwwdropboxcomhelp167-to-a-file-or-folderdropbox-for-business-u",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.dropbox.com",
              "path": [
                "1",
                "shares/:root/:path"
              ],
              "variable": [
                {
                  "id": "path",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "root",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "POST",
            "body": {
              "mode": "urlencoded",
              "urlencoded": [
                {
                  "key": "locale",
                  "value": "{}",
                  "disabled": false,
                  "description": "Use to specify language settings for user error messages and other language specific text"
                },
                {
                  "key": "short_url",
                  "value": "{}",
                  "disabled": false,
                  "description": "When `true` (default), the URL returned will be shortened using the Dropbox URL shortener"
                }
              ]
            },
            "description": "Creates and returns a [shared link](https://www.dropbox.com/help/167) to a file or folder.\n\nDropbox for Business users can set restrictions on shared links; the `visibility` field indicates what\n(if any) restrictions are set on this particular link. Possible values include:\n  * `PUBLIC` - anyone can view\n  * `TEAM_ONLY` - only the owner's team can view\n  * `PASSWORD` - a password is required\n  * `TEAM_AND_PASSWORD` - a combination of `TEAM_ONLY` and `PASSWORD` restrictions\n  * `SHARED_FOLDER_ONLY` - only [members](https://www.dropbox.com/help/6636) of the enclosing shared folder can view\n\nNote that other values may be added at any time."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "0bdc2099-c763-45ad-928d-9168097b62f8"
            }
          ]
        },
        {
          "id": "c9978885-9cf1-4655-aad4-8f1a90d8653e",
          "name": "returns-a-link-directly-to-a-filesimilar-to-shareshttpswwwdropboxcomdeveloperscoredocsshares-the-dif",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.dropbox.com",
              "path": [
                "1",
                "media/:root/:path"
              ],
              "variable": [
                {
                  "id": "path",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "root",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "POST",
            "body": {
              "mode": "urlencoded",
              "urlencoded": [
                {
                  "key": "locale",
                  "value": "{}",
                  "disabled": false,
                  "description": "Use to specify language settings for user error messages and other language specific text"
                }
              ]
            },
            "description": "Returns a link directly to a file.\n\nSimilar to [/shares](https://www.dropbox.com/developers/core/docs#shares). The difference is that this\nbypasses the Dropbox webserver, used to provide a preview of the file, so that you can effectively stream\nthe contents of your media. This URL should not be used to display content directly in the browser.\n\nThe `/media` link expires after four hours, allotting enough time to stream files, but not enough to leave\na connection open indefinitely."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "dbe60a16-385f-405e-94e6-844f2b1fb5d9"
            }
          ]
        },
        {
          "id": "5aa05bc3-0982-49be-a757-52a0484cd21e",
          "name": "creates-and-returns-a-copy-ref-to-a-filethis-reference-string-can-be-used-to-copy-that-file-to-anoth",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.dropbox.com",
              "path": [
                "1",
                "copy_ref/:root/:path"
              ],
              "variable": [
                {
                  "id": "path",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "root",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Creates and returns a `copy_ref` to a file.\n\nThis reference string can be used to copy that file to another user's Dropbox by passing it in as the\n`from_copy_ref` parameter on [/fileops/copy](https://www.dropbox.com/developers/core/docs#fileops-copy)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "7f28d8dc-9cfb-44b9-a967-5e765a4266ed"
            }
          ]
        },
        {
          "id": "f76df9b4-cb42-463c-81b7-138cdbee6919",
          "name": "returns-a-list-of-all-shared-folders-the-authenticated-user-has-access-tothis-api-call-requires-full",
          "request": {
            "url": "http://api.dropbox.com/1/shared_folders?include_membership=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns a list of all shared folders the authenticated user has access to.\n\nThis API call requires Full Dropbox or File type [permissions](https://www.dropbox.com/developers/reference/devguide#app-permissions).\n\nNote that `same_team` is only present if the linked account is a member of a Dropbox for Business team,\nand `member_id` is only present when this endpoint is called by a Dropbox for Business app and the user\nis on that team.\n\nThe `membership` field only contains users who have joined the shared folder and does not include users who\nhave been invited but have not accepted. When the `active` field is `false`, it means that a user has left\na shared folder (but may still rejoin)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "aaed1774-8dd8-4060-861c-f11bb1361477"
            }
          ]
        },
        {
          "id": "e7bfcb9b-26cf-470d-a552-92367c83106a",
          "name": "returns-metadata-about-a-specific-shared-folderthis-api-call-requires-full-dropbox-or-file-type-perm",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.dropbox.com",
              "path": [
                "1",
                "shared_folders/:shared_folder_id"
              ],
              "query": [
                {
                  "key": "include_membership",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "shared_folder_id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns metadata about a specific shared folder.\n\nThis API call requires Full Dropbox or File type [permissions](https://www.dropbox.com/developers/reference/devguide#app-permissions).\n\nNote that `same_team` is only present if the linked account is a member of a Dropbox for Business team,\nand `member_id` is only present when this endpoint is called by a Dropbox for Business app and the user\nis on that team.\n\nThe `membership` field only contains users who have joined the shared folder and does not include users who\nhave been invited but have not accepted. When the `active` field is `false`, it means that a user has left\na shared folder (but may still rejoin)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ced87876-6ed7-484e-ab5f-b9b37bbd12ee"
            }
          ]
        },
        {
          "id": "652267f9-fd9e-48c5-9b05-b218f3378b17",
          "name": "save-a-file-from-the-specified-url-into-dropboxif-the-given-path-already-exists-the-file-will-be-ren",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.dropbox.com",
              "path": [
                "1",
                "save_url/:root/:path"
              ],
              "variable": [
                {
                  "id": "path",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "root",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "POST",
            "body": {
              "mode": "urlencoded",
              "urlencoded": [
                {
                  "key": "url",
                  "value": "{}",
                  "disabled": false,
                  "description": "The URL to be fetched"
                }
              ]
            },
            "description": "Save a file from the specified URL into Dropbox.\n\nIf the given path already exists, the file will be renamed to avoid the conflict (e.g. `myfile (1).txt`)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f77b1fcd-9a00-4596-8bcc-30bcec10b4e1"
            }
          ]
        },
        {
          "id": "abfd4750-4ae1-4158-9e00-5e29f7535e07",
          "name": "check-the-status-of-a-save-urlhttpswwwdropboxcomdeveloperscoredocssaveurl-jobstatus-field-may-have-o",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.dropbox.com",
              "path": [
                "1",
                "save_url_job/:job-id"
              ],
              "variable": [
                {
                  "id": "job-id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Check the status of a [save URL](https://www.dropbox.com/developers/core/docs#save-url) job.\n\nStatus field may have one of the following values:\n  * `PENDING` – The job has not yet started.\n  * `DOWNLOADING` – The job has started but hasn't yet completed.\n  * `COMPLETE` – The job is complete.\n  * `FAILED` – The job failed. An additional `error` field will describe the failure."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "aedbd023-30be-4e4c-989b-30344d499160"
            }
          ]
        },
        {
          "id": "6951a355-3bb7-4bfd-aaaa-481b09fff343",
          "name": "copies-a-file-or-folder-to-a-new-location",
          "request": {
            "url": "http://api.dropbox.com/1/fileops/copy",
            "method": "POST",
            "body": {
              "mode": "urlencoded",
              "urlencoded": [
                {
                  "key": "from_copy_ref",
                  "value": "{}",
                  "disabled": false,
                  "description": "Specifies a `copy_ref` generated from a previous [/copy_ref](https://www"
                },
                {
                  "key": "from_path",
                  "value": "{}",
                  "disabled": false,
                  "description": "Specifies the file or folder to be copied from relative to `root`"
                },
                {
                  "key": "locale",
                  "value": "{}",
                  "disabled": false,
                  "description": "The metadata returned will have its `size` field translated based on the given locale"
                },
                {
                  "key": "root",
                  "value": "{}",
                  "disabled": false,
                  "description": "The root relative to which `from_path` and `to_path` are specified"
                },
                {
                  "key": "to_path",
                  "value": "{}",
                  "disabled": false,
                  "description": "Specifies the destination path, *including the new name for the file or folder*, relative to `root`"
                }
              ]
            },
            "description": "Copies a file or folder to a new location."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "bbc944c1-ecaa-4bab-a3a4-2662606822a2"
            }
          ]
        },
        {
          "id": "55c084d9-0c8e-459b-9ae8-040c92677236",
          "name": "creates-a-folder",
          "request": {
            "url": "http://api.dropbox.com/1/fileops/create_folder",
            "method": "POST",
            "body": {
              "mode": "urlencoded",
              "urlencoded": [
                {
                  "key": "locale",
                  "value": "{}",
                  "disabled": false,
                  "description": "The metadata returned will have its `size` field translated based on the given locale"
                },
                {
                  "key": "path",
                  "value": "{}",
                  "disabled": false,
                  "description": "The path to the new folder to create relative to `root`"
                },
                {
                  "key": "root",
                  "value": "{}",
                  "disabled": false,
                  "description": "The root relative to which `path` is specified"
                }
              ]
            },
            "description": "Creates a folder."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3e953fff-6d1c-4669-85aa-e088fbd5001f"
            }
          ]
        },
        {
          "id": "3c79010f-3b44-4cc2-897f-0b7bdd3f4ce6",
          "name": "deletes-a-file-or-folder",
          "request": {
            "url": "http://api.dropbox.com/1/fileops/delete",
            "method": "POST",
            "body": {
              "mode": "urlencoded",
              "urlencoded": [
                {
                  "key": "locale",
                  "value": "{}",
                  "disabled": false,
                  "description": "The metadata returned will have its `size` field translated based on the given locale"
                },
                {
                  "key": "path",
                  "value": "{}",
                  "disabled": false,
                  "description": "The path to the file or folder to be deleted"
                },
                {
                  "key": "root",
                  "value": "{}",
                  "disabled": false,
                  "description": "The root relative to which `path` is specified"
                }
              ]
            },
            "description": "Deletes a file or folder."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ad31620d-14cc-4ba9-a407-05949f65d3d3"
            }
          ]
        }
      ]
    }
  ]
}