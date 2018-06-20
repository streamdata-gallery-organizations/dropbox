{
  "info": {
    "name": "Dropbox Datastore API OAuth Token",
    "_postman_id": "764739fb-6dd8-42f8-96c3-7551a3f2ddaa",
    "description": "/oauth2/token",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Chunked",
      "item": [
        {
          "id": "52adf488-7530-47d9-a0b7-6add77560a7c",
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
              "id": "061f69fd-1def-4b00-a30d-fc6302f61703"
            }
          ]
        }
      ]
    },
    {
      "name": "Delta",
      "item": [
        {
          "id": "dd296826-2432-4a87-af6a-51157b87e9f6",
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
              "id": "4dea9682-795d-443b-8f98-9aa6ddbcf327"
            }
          ]
        }
      ]
    },
    {
      "name": "Disable",
      "item": [
        {
          "id": "fb7a2fd6-3017-406c-b8e5-6a3dfd27474f",
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
              "id": "e47b689f-c30e-4e7a-8a3d-77a327f8bea5"
            }
          ]
        }
      ]
    },
    {
      "name": "Fileops",
      "item": [
        {
          "id": "62902e1f-c5a6-4185-8bf5-c8caad896026",
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
              "id": "5e999f5e-5d9a-4cf0-8b4a-19e636872f03"
            }
          ]
        }
      ]
    },
    {
      "name": "Files",
      "item": [
        {
          "id": "e47d1ffe-9bc3-4dbf-8d08-37c1fe26dfd0",
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
              "id": "dafabdab-6c34-43e6-b200-d419b24e7da3"
            }
          ]
        }
      ]
    },
    {
      "name": "Media",
      "item": [
        {
          "id": "17a7605a-6744-4f7a-a382-94ed6c0fe37b",
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
              "id": "e974c2cc-5c85-4944-b2e3-ac98ee3be6a7"
            }
          ]
        }
      ]
    },
    {
      "name": "Metadata",
      "item": [
        {
          "id": "e5549923-32b3-45c6-bc25-38c992e4295a",
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
              "id": "a043733b-2530-428c-86b0-b39faee8f2f9"
            }
          ]
        }
      ]
    },
    {
      "name": "Oauth",
      "item": [
        {
          "id": "70845c12-5e5a-4b3e-aba6-0d69366143f3",
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
              "id": "762d4c5e-de0c-4cde-b2b5-b040753d0947"
            }
          ]
        },
        {
          "id": "dda8b35b-c54f-4fa9-bb40-ea9967fd1621",
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
              "id": "7a28ead5-90b5-4c07-bc50-64451db05927"
            }
          ]
        }
      ]
    },
    {
      "name": "Oauth2",
      "item": [
        {
          "id": "be2945a7-0c9c-486d-9e1b-989fcc64ea0c",
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
              "id": "5362d63d-fb3a-42f0-b0b8-3e94a450217b"
            }
          ]
        }
      ]
    }
  ]
}