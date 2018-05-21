{
  "info": {
    "name": "Dropbox Core Disables the access token.",
    "_postman_id": "4e6841fd-8b18-4644-8ed8-e86f1b3d4b1d",
    "description": "Disables the access token used to authenticate the call. This method works for OAuth 1 and OAuth 2 tokens.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Storage",
      "item": [
        {
          "id": "65c59c58-186e-40c2-90f3-5e870ad1fa7d",
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
              "id": "7942fc72-e4f6-403f-8dd0-b9ad925beb73"
            }
          ]
        },
        {
          "id": "a85780d9-01f9-40bf-b23d-0279ac15dd89",
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
              "id": "fa9314ef-00a3-4083-84b5-5e49523542e5"
            }
          ]
        }
      ]
    }
  ]
}