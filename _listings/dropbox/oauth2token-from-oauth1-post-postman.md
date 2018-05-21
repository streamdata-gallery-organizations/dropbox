{
  "info": {
    "name": "Dropbox Core Convert OAuth 1 token to OAuth 2 token.",
    "_postman_id": "a811376d-53b0-4d4d-892c-e0121d167a4c",
    "description": "This endpoint should be used by apps transitioning from OAuth 1 to OAuth 2. It will return an OAuth 2 token\nfor the authenticated user.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Storage",
      "item": [
        {
          "id": "bf91c808-dbf6-4b3b-b38d-c43fdd302c8a",
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
              "id": "e5dd34f7-5c54-4b33-8825-636feb41543a"
            }
          ]
        }
      ]
    }
  ]
}