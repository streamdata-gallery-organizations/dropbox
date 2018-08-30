{
  "info": {
    "name": "Dropbox Datastore API Get Revisions",
    "_postman_id": "46b42da2-e36b-4392-ae2c-22c61b656541",
    "description": "/revisions",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Chunked",
      "item": [
        {
          "id": "b9e5f1fd-59d0-44cf-a38e-cd84d3f73df7",
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
              "id": "080ccc1b-02b8-4ddb-bdba-7b6c1bbcec1b"
            }
          ]
        }
      ]
    },
    {
      "name": "Delta",
      "item": [
        {
          "id": "89244443-ed65-48a5-97a8-4bd537b454f4",
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
              "id": "f0b324b3-01fb-43d5-89de-17e169aaa0a6"
            }
          ]
        }
      ]
    },
    {
      "name": "Disable",
      "item": [
        {
          "id": "5209ede8-ac03-4e64-91c2-6e1896b31070",
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
              "id": "a2bb2cb8-7149-4774-bcd7-4378f37a8d47"
            }
          ]
        }
      ]
    },
    {
      "name": "Fileops",
      "item": [
        {
          "id": "d3c40bb4-97d3-4c68-8f69-ef9147644a06",
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
              "id": "d1a59c44-8ecf-4c8b-8718-8fe3c076fbad"
            }
          ]
        }
      ]
    },
    {
      "name": "Files",
      "item": [
        {
          "id": "5a0417f0-c840-456f-a9fa-00e19b9aa47c",
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
              "id": "fdca3775-a7e2-4385-9784-8e7813f414b4"
            }
          ]
        }
      ]
    },
    {
      "name": "Media",
      "item": [
        {
          "id": "384819f6-6b02-42d9-9a33-f381ea3dec3d",
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
              "id": "d8199804-1394-4a9b-bd23-ad13ac5c72ff"
            }
          ]
        }
      ]
    },
    {
      "name": "Metadata",
      "item": [
        {
          "id": "dd30b766-4c1d-4743-b323-6ccd0816d92c",
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
              "id": "58739bcf-aab5-4e08-93d1-3aa9d7358c0b"
            }
          ]
        }
      ]
    },
    {
      "name": "Oauth",
      "item": [
        {
          "id": "c1f28df0-ab1e-40ba-91ab-daad747e9d43",
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
              "id": "2ba812cc-2087-4f43-9f6d-6cc3826de27c"
            }
          ]
        },
        {
          "id": "16d1c9f6-8a4e-411a-8320-a4e8ee6a65ae",
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
              "id": "ebbfb5f7-240d-4443-a5f4-29bf72526c34"
            }
          ]
        }
      ]
    },
    {
      "name": "Oauth2",
      "item": [
        {
          "id": "74030554-3615-4930-8969-52fc9460dd79",
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
              "id": "2eb1100e-4e55-42b6-b483-58163fbe2aa2"
            }
          ]
        }
      ]
    },
    {
      "name": "Revisions",
      "item": [
        {
          "id": "bd64eb86-f4ae-466c-9275-c176eaee3da9",
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
              "id": "3720ea38-83b5-4079-a77c-07aef0a6b08e"
            }
          ]
        }
      ]
    }
  ]
}