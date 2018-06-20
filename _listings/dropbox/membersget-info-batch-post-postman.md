{
  "info": {
    "name": "Cloud Elements - Dropbox For Business API Get Info Batch",
    "_postman_id": "a26dd9ea-7326-4767-92a5-078fb70d8dfc",
    "description": "Get info batch.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Info",
      "item": [
        {
          "id": "f2442d2e-771a-4d03-ba28-6e934767ee1e",
          "name": "postMembersGetInfoBatch",
          "request": {
            "url": "http://api.dropbox.com/1/team/members/get_info_batch?emails=%7B%7D&external_ids=%7B%7D&member_ids=%7B%7D",
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "Get info batch."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "736dcaaa-bbd4-4dc9-95bd-0ee114506993"
            }
          ]
        }
      ]
    }
  ]
}