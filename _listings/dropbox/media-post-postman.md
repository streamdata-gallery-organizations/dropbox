{
  "info": {
    "name": "Dropbox Datastore API Add Media",
    "_postman_id": "2fdfc95a-3b42-4167-82d5-a249ccb7df82",
    "description": "/media",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Chunked",
      "item": [
        {
          "id": "c76e72df-4713-4017-83e1-cfdf202490a7",
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
              "id": "8e8c48f7-139c-4e18-afb3-f3952e1efa07"
            }
          ]
        }
      ]
    },
    {
      "name": "Delta",
      "item": [
        {
          "id": "7cb80c4a-bf99-489e-a64b-038cb021745b",
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
              "id": "67d1780e-8f26-4119-a9a4-588ad3045e73"
            }
          ]
        }
      ]
    },
    {
      "name": "Disable",
      "item": [
        {
          "id": "28672af2-62b1-45a3-9fad-2e0ad91484e4",
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
              "id": "e3a457d5-0731-4e00-9e2d-2fc514e62342"
            }
          ]
        }
      ]
    },
    {
      "name": "Fileops",
      "item": [
        {
          "id": "1510771b-59af-4138-be09-3f44252bae9e",
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
              "id": "613d7833-222e-4e76-b8a1-e501bef21c68"
            }
          ]
        }
      ]
    },
    {
      "name": "Files",
      "item": [
        {
          "id": "5b881a2e-dc14-4c90-86cf-06d36faf08ff",
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
              "id": "6e477ac4-e1b4-406d-8aa8-fb5eceb7091c"
            }
          ]
        }
      ]
    },
    {
      "name": "Media",
      "item": [
        {
          "id": "d61209fd-eb78-43a4-8214-9b3ede38a063",
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
              "id": "b5bd6ccf-f41a-4a46-87c7-639e6a255561"
            }
          ]
        }
      ]
    }
  ]
}