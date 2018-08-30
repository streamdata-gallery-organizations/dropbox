{
  "info": {
    "name": "Dropbox Datastore API OAuth Access Token",
    "_postman_id": "8b3964fe-9e27-439f-bc2b-72d83685e46b",
    "description": "/oauth/access_token",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Disable",
      "item": [
        {
          "id": "f837f9e3-bdbc-4c62-91d6-d802401bf3c2",
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
              "id": "8b9c1212-ac04-453e-b539-f9cfe466a417"
            }
          ]
        }
      ]
    },
    {
      "name": "Oauth",
      "item": [
        {
          "id": "a1232542-8f78-4e56-bef3-5260b1ae4cc1",
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
              "id": "d0a5d85e-dff9-49e5-b469-531a45a7c1bb"
            }
          ]
        }
      ]
    }
  ]
}