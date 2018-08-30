{
  "info": {
    "name": "Dropbox Datastore API OAuth Request Token",
    "_postman_id": "c8ef4586-d295-4883-9a88-5736d416a74a",
    "description": "/oauth/request_token",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Chunked",
      "item": [
        {
          "id": "20fe947b-c176-450a-b887-61f2f36ee8a8",
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
              "id": "361fb343-0627-4b89-aca8-9a62c9ca57cf"
            }
          ]
        }
      ]
    },
    {
      "name": "Delta",
      "item": [
        {
          "id": "6a4ca81a-a132-4581-8034-48fd8d58a268",
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
              "id": "7c85b8a9-d5d2-47d3-9c69-c5e38e372c8a"
            }
          ]
        }
      ]
    },
    {
      "name": "Disable",
      "item": [
        {
          "id": "cc11abcf-357f-4d1c-bfb2-d503415da682",
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
              "id": "fc4eaeda-cb4a-4a30-b7ac-a28801726ef8"
            }
          ]
        }
      ]
    },
    {
      "name": "Fileops",
      "item": [
        {
          "id": "3516b4fc-2005-4f7d-86ef-306f53d42311",
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
              "id": "677e1873-1321-4305-8d1e-825d08652e1e"
            }
          ]
        }
      ]
    },
    {
      "name": "Files",
      "item": [
        {
          "id": "d6456780-9999-41c3-93bd-604811e23ad2",
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
              "id": "569daefc-dfc3-4482-87d5-d5c33bf47932"
            }
          ]
        }
      ]
    },
    {
      "name": "Media",
      "item": [
        {
          "id": "3614fe53-6d85-41ef-9800-808af99967eb",
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
              "id": "3605c32f-22e5-468a-a4fc-23efaf183852"
            }
          ]
        }
      ]
    },
    {
      "name": "Metadata",
      "item": [
        {
          "id": "c53f5225-c355-4a5a-9f26-78bc63c4b26a",
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
              "id": "41a76da8-bee9-40e1-a078-ae4d4700e87b"
            }
          ]
        }
      ]
    },
    {
      "name": "Oauth",
      "item": [
        {
          "id": "34d3dd11-c005-4e63-b1a5-3a8777e0281d",
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
              "id": "bd641627-cec7-41c5-8aa6-881c67e1141f"
            }
          ]
        },
        {
          "id": "4e5d9b2e-b948-40a7-b244-6db7581a6159",
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
              "id": "5d7ff3d3-5886-4731-9122-b861ce14951e"
            }
          ]
        }
      ]
    }
  ]
}