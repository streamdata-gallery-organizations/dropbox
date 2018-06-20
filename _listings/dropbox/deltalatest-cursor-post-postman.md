{
  "info": {
    "name": "Dropbox Datastore API Latest Cursor",
    "_postman_id": "21c477cd-23d4-49d1-ad37-d2a06389a7d3",
    "description": "/delta/latest_cursor",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Chunked",
      "item": [
        {
          "id": "3d6917e6-5512-4f94-950a-a6fc9043233a",
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
              "id": "3a163556-ba9a-4f61-974a-82c03077c244"
            }
          ]
        }
      ]
    },
    {
      "name": "Delta",
      "item": [
        {
          "id": "edbef224-3613-4672-b757-1d2935605ded",
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
              "id": "f1c20867-4e94-4576-be66-f7db62c664b4"
            }
          ]
        }
      ]
    }
  ]
}