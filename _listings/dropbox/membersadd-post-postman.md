{
  "info": {
    "name": "Cloud Elements - Dropbox For Business API Add Member",
    "_postman_id": "ec43a2b9-750e-4480-86e9-781371ebb958",
    "description": "Add member.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Info",
      "item": [
        {
          "id": "252e39a3-b81e-4a48-9139-8d9060b9da2e",
          "name": "postGetInfo",
          "request": {
            "url": "http://api.dropbox.com/1/team/get_info",
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "Get info."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "92459577-8c9c-43ce-8730-eebc79859e5e"
            }
          ]
        }
      ]
    },
    {
      "name": "Events",
      "item": [
        {
          "id": "1c6179dc-3526-4b25-aa0a-67632697b52b",
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
              "id": "226241e3-fd9f-4e36-acbb-1f726d32dae9"
            }
          ]
        }
      ]
    },
    {
      "name": "Member",
      "item": [
        {
          "id": "532abefc-a95c-4220-8807-25e0678e5ba2",
          "name": "postMembersAdd",
          "request": {
            "url": "http://api.dropbox.com/1/team/members/add?member_email=%7B%7D&member_external_id=%7B%7D&member_given_name=%7B%7D&member_surname=%7B%7D&send_welcome_email=%7B%7D",
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "Add member."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "bcc02169-595e-46b2-8717-95ff69c06a37"
            }
          ]
        }
      ]
    }
  ]
}