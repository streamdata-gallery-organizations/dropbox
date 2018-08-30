{
  "info": {
    "name": "Dropbox Datastore API Get File",
    "_postman_id": "35465432-da23-406e-8a5c-94ef584f2ec1",
    "description": "/files (GET)",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Files",
      "item": [
        {
          "id": "1bce7491-4922-41f2-a59e-7e091288cfac",
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
              "id": "525b38d1-31ce-4aa7-9075-772a8f744be3"
            }
          ]
        }
      ]
    }
  ]
}