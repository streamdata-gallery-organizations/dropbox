{
  "info": {
    "name": "Dropbox Datastore API Create Folder",
    "_postman_id": "84db1956-0116-431f-a6b9-92f5a02e2198",
    "description": "/fileops/create_folder",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Chunked",
      "item": [
        {
          "id": "af123e9c-a410-4cf4-8f55-f08c118775da",
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
              "id": "b5715e20-da04-4984-af71-75da5a588bad"
            }
          ]
        }
      ]
    },
    {
      "name": "Delta",
      "item": [
        {
          "id": "617b3cb6-bf0b-4edd-a801-5e679cec282c",
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
              "id": "3fd03d5a-0181-4f0f-8f9b-6c8d13e9225b"
            }
          ]
        }
      ]
    },
    {
      "name": "Disable",
      "item": [
        {
          "id": "f3fc9ff3-025f-4f2c-870e-bdf6b0dd62a3",
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
              "id": "3b027c32-9575-4b7d-80b4-7d668cfeba4b"
            }
          ]
        }
      ]
    },
    {
      "name": "Fileops",
      "item": [
        {
          "id": "ef80e4e4-a7ee-4b50-b28d-d6046a09a8bc",
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
              "id": "fdd9997f-05cb-48cd-b19f-52bf6dfc0f37"
            }
          ]
        }
      ]
    }
  ]
}