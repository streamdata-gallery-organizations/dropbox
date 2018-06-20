{
  "info": {
    "name": "Dropbox Datastore API Chunked Upload",
    "_postman_id": "6f5be355-e9fc-40ca-91c1-258a79e2e469",
    "description": "/chunked_upload",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Chunked",
      "item": [
        {
          "id": "d6515d23-a6ab-4b94-a4f7-c5c05abfba43",
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
              "id": "2d8555c4-8929-4774-bfc1-65b3dd590f10"
            }
          ]
        }
      ]
    }
  ]
}