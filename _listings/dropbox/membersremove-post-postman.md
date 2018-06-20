{
  "info": {
    "name": "Cloud Elements - Dropbox For Business API Remove",
    "_postman_id": "4f37ad95-e3f9-42f5-bf70-326bfafd8947",
    "description": "Remove.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Info",
      "item": [
        {
          "id": "5fbd44b0-f577-4910-8cb1-ac1c3f4101c3",
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
              "id": "40d9689b-2e53-4258-a684-1f450836c115"
            }
          ]
        },
        {
          "id": "60e3754c-f85e-4c1c-b347-be9cb2550408",
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
              "id": "16ad9c99-dbed-49b9-a49f-d48c675bbb75"
            }
          ]
        }
      ]
    },
    {
      "name": "Events",
      "item": [
        {
          "id": "9c22e385-b4b1-4d0e-b796-0234813fde07",
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
              "id": "b3662fb0-67f1-493f-a09a-8f25216d92c7"
            }
          ]
        }
      ]
    },
    {
      "name": "Member",
      "item": [
        {
          "id": "9dfabeba-c66e-4fba-a97c-75e0f27f1b4f",
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
              "id": "f7eddfd8-981e-4077-ada2-378997b71972"
            }
          ]
        },
        {
          "id": "2f10244e-53d8-46c0-8bf6-40b80380f5f5",
          "name": "postMembersGetInfo",
          "request": {
            "url": "http://api.dropbox.com/1/team/members/get_info?email=%7B%7D&external_id=%7B%7D&member_id=%7B%7D",
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "Get member info."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "647cec56-7220-46ef-8235-8b5135276714"
            }
          ]
        }
      ]
    },
    {
      "name": "List",
      "item": [
        {
          "id": "1a4083a1-2666-42a3-aca1-a9e0cb64d1cb",
          "name": "postMembersList",
          "request": {
            "url": "http://api.dropbox.com/1/team/members/list?cursor=%7B%7D&limit=%7B%7D",
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "List members."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "445e5ee1-5b89-4bb4-b9e8-f7a1cfbe37c1"
            }
          ]
        }
      ]
    },
    {
      "name": "Remove",
      "item": [
        {
          "id": "c75651fc-3759-48a7-b028-8091769ca9e2",
          "name": "postMembersRemove",
          "request": {
            "url": "http://api.dropbox.com/1/team/members/remove?delete_data=%7B%7D&external_id=%7B%7D&member_id=%7B%7D&transfer_admin_member_id=%7B%7D&transfer_dest_member_id=%7B%7D",
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "Remove."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e6794e7b-f0f1-443c-ab3c-2ad332b63ccb"
            }
          ]
        }
      ]
    }
  ]
}