{
  "info": {
    "name": "Cloud Elements - Dropbox For Business API Get Events",
    "_postman_id": "3c526d93-0d64-448a-bfb5-466efa9cc986",
    "description": "Get events.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Events",
      "item": [
        {
          "id": "1c361d53-6da9-4bed-85bc-489c6661fd0f",
          "name": "postLogGetEvents",
          "request": {
            "url": "http://api.dropbox.com/1/team/log/get_events?category=%7B%7D&cursor=%7B%7D&end_ts=%7B%7D&limit=%7B%7D&start_ts=%7B%7D&user=%7B%7D",
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "Get events."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "1cd5fcd0-7c9a-427f-81ac-297e2554925e"
            }
          ]
        }
      ]
    }
  ]
}