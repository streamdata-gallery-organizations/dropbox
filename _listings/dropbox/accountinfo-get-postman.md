{
  "info": {
    "name": "Dropbox Core Retrieves information about the user's account.",
    "_postman_id": "49de3feb-6ddd-4874-b038-2ec691b6caeb",
    "description": "Retrieves information about the user's account.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Storage",
      "item": [
        {
          "id": "c20c3dc2-bceb-4da5-a1df-ce40699b31a0",
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
              "id": "653b9cdb-e942-49b1-8730-b630894ed8f0"
            }
          ]
        },
        {
          "id": "24e1e68c-eb44-40a9-bb24-e6ff78ccffb5",
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
              "id": "4f9009e1-078e-491e-a313-86ee0b28894c"
            }
          ]
        },
        {
          "id": "d3c64f51-37be-4fe0-a190-8c73f0e389e5",
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
              "id": "a4f6e8cc-22d3-4a40-bdba-58666f626a4d"
            }
          ]
        }
      ]
    }
  ]
}