{
  "info": {
    "name": "Dropbox Datastore API Shared Folders",
    "_postman_id": "43943258-2e9c-41ef-9e62-9f9c8e5d0b62",
    "description": "/shared_folders",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Shared",
      "item": [
        {
          "id": "3d04cfea-dd7a-4cbf-9d04-2f5461109874",
          "name": "shared-folders",
          "request": {
            "url": "http://api.dropbox.com/1/shared_folders?id=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "/shared_folders"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8a224beb-8559-4a8c-9e92-bf249d2da112"
            }
          ]
        }
      ]
    }
  ]
}