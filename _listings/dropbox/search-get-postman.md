{
  "info": {
    "name": "Dropbox Datastore API Search",
    "_postman_id": "57f57952-2e9d-45ac-818d-a69d519628f7",
    "description": "/search",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Chunked",
      "item": [
        {
          "id": "7d129a77-0d7a-4b5f-adf9-86d749d4b057",
          "name": "chunked-upload",
          "request": {
            "url": "http://api.dropbox.com/1/chunked_upload?offset=%7B%7D&upload_id=%7B%7D",
            "method": "PUT",
            "body": {
              "mode": "raw"
            },
            "description": "/chunked_upload"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "0efc28a8-4920-40ea-b8b4-3465b33d11a1"
            }
          ]
        }
      ]
    },
    {
      "name": "Delta",
      "item": [
        {
          "id": "3769be56-0f7b-4dea-aa90-5d45cc0ff884",
          "name": "deltalatest-cursor",
          "request": {
            "url": "http://api.dropbox.com/1/delta/latest_cursor?include_media_info=%7B%7D&path_prefix=%7B%7D",
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "/delta/latest_cursor"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "0f0727ea-5588-4bea-92f5-c3ba5f412ac7"
            }
          ]
        }
      ]
    },
    {
      "name": "Disable",
      "item": [
        {
          "id": "e1111457-9c2a-4914-8380-4a1f34be914f",
          "name": "disable-access-token",
          "request": {
            "url": "http://api.dropbox.com/1/disable_access_token",
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "/disable_access_token"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "925fa2b3-ffe9-4e0b-9e35-ae04c1a2103e"
            }
          ]
        }
      ]
    },
    {
      "name": "Fileops",
      "item": [
        {
          "id": "8c7a791b-9afa-4480-ac46-e118521ed052",
          "name": "fileopscreate-folder",
          "request": {
            "url": "http://api.dropbox.com/1/fileops/create_folder?locale=%7B%7D&path=%7B%7D&root=%7B%7D",
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "/fileops/create_folder"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a9be5899-78c4-49ba-8ad6-b65eeaca1c2a"
            }
          ]
        }
      ]
    },
    {
      "name": "Files",
      "item": [
        {
          "id": "bf0ae1a9-994d-4ee5-9ef2-f2a4bf851e13",
          "name": "files-get",
          "request": {
            "url": "http://api.dropbox.com/1/files?path=%7B%7D&rev=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "/files (GET)"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "008b3371-824b-48fa-af03-418bf0682bb2"
            }
          ]
        }
      ]
    },
    {
      "name": "Media",
      "item": [
        {
          "id": "0d9de380-3a56-4555-b298-59da44736aba",
          "name": "media",
          "request": {
            "url": "http://api.dropbox.com/1/media?locale=%7B%7D",
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "/media"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "59403ef7-d01a-41a2-af9e-90cf9b1a9138"
            }
          ]
        }
      ]
    },
    {
      "name": "Metadata",
      "item": [
        {
          "id": "3d9a249a-fe97-4888-8b50-712e57ee4af8",
          "name": "metadata",
          "request": {
            "url": "http://api.dropbox.com/1/metadata?file_limit=%7B%7D&hash=%7B%7D&include_deleted=%7B%7D&include_media_info=%7B%7D&include_membership=%7B%7D&list=%7B%7D&locale=%7B%7D&rev=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "/metadata"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "0bdd0120-f129-4297-9657-7b991f2683a8"
            }
          ]
        }
      ]
    },
    {
      "name": "Oauth",
      "item": [
        {
          "id": "092b4d8b-4adc-4657-b6a3-633e6002bf8b",
          "name": "oauthaccess-token",
          "request": {
            "url": "http://api.dropbox.com/1/oauth/access_token",
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "/oauth/access_token"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8a4646d6-32d6-4e53-a671-da893f222fbb"
            }
          ]
        },
        {
          "id": "66dbfb5c-5efc-4415-af8f-dafbad5d82f6",
          "name": "oauthrequest-token",
          "request": {
            "url": "http://api.dropbox.com/1/oauth/request_token",
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "/oauth/request_token"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "362caf49-6187-4c4e-96bd-600293292dee"
            }
          ]
        }
      ]
    },
    {
      "name": "Oauth2",
      "item": [
        {
          "id": "7cf46f98-83fa-40ae-8479-a60374b0a196",
          "name": "oauth2token",
          "request": {
            "url": "http://api.dropbox.com/1/oauth2/token?client_id=%7B%7D&client_secret=%7B%7D&code=%7B%7D&grant_type=%7B%7D&redirect_uri=%7B%7D",
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "/oauth2/token"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d83b9233-b7e7-4f3b-86c4-c16589e48436"
            }
          ]
        }
      ]
    },
    {
      "name": "Revisions",
      "item": [
        {
          "id": "d4d6fa8c-f468-4e42-8f62-4456b5ec7278",
          "name": "revisions",
          "request": {
            "url": "http://api.dropbox.com/1/revisions?locale=%7B%7D&rev_limit=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "/revisions"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "2cf595eb-0d5c-4efa-905b-d09abd9fa8c7"
            }
          ]
        }
      ]
    },
    {
      "name": "Search",
      "item": [
        {
          "id": "8e3959bb-5720-419d-800f-ca4582cfbf56",
          "name": "search",
          "request": {
            "url": "http://api.dropbox.com/1/search?file_limit=%7B%7D&include_deleted=%7B%7D&include_membership=%7B%7D&locale=%7B%7D&query=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "/search"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "6226947d-4c0e-4aaf-8ad3-67341838f3e9"
            }
          ]
        }
      ]
    }
  ]
}