{
  "info": {
    "name": "Dropbox Datastore API Get Meta Data",
    "_postman_id": "27a68167-0249-4aa2-a2ec-6de0b5fbe014",
    "description": "/metadata",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Metadata",
      "item": [
        {
          "id": "54a9fc8f-4763-4797-85a6-07f1c44b02c1",
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
              "id": "5122486d-76cc-4835-8f2d-7311317ecd18"
            }
          ]
        }
      ]
    }
  ]
}