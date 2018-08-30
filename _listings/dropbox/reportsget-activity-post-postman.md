{
  "info": {
    "name": "Cloud Elements - Dropbox For Business API Get Activity",
    "_postman_id": "35b60bc7-1b1c-401f-853c-35bbd92b6331",
    "description": "Get activity.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Info",
      "item": [
        {
          "id": "6d90bcef-f16f-46e5-8e3c-054794e86af1",
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
              "id": "ec36a102-d6bb-4cba-9f4c-093bdf159f8d"
            }
          ]
        },
        {
          "id": "af99d812-c158-4ccc-810f-e7b0454f7155",
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
              "id": "010d3525-198d-406d-847b-9e70f18581a3"
            }
          ]
        }
      ]
    },
    {
      "name": "Events",
      "item": [
        {
          "id": "d4b4e048-8ea5-4e61-926c-f34af6fa291b",
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
              "id": "28d842d1-6136-47a7-b094-8272738e9231"
            }
          ]
        }
      ]
    },
    {
      "name": "Member",
      "item": [
        {
          "id": "962a7b9f-3492-4c70-930e-574d5960596a",
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
              "id": "d5e84dcc-a7b6-480a-bfce-65d04b41fdff"
            }
          ]
        },
        {
          "id": "e9fd1707-c906-460f-b895-f9d4c4841321",
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
              "id": "a167bf7e-2e5d-41fa-9f4a-d63ab39231b1"
            }
          ]
        }
      ]
    },
    {
      "name": "List",
      "item": [
        {
          "id": "1f8c5ae4-65a6-4bd8-9bc3-8341c4adc500",
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
              "id": "9bf3241c-7513-443a-beb4-56ce3ea4fc4e"
            }
          ]
        }
      ]
    },
    {
      "name": "Remove",
      "item": [
        {
          "id": "c3dd27f0-b7c1-439e-b5e9-cfe29b509b81",
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
              "id": "1366251b-ee4f-4d5b-9458-d0272ee54638"
            }
          ]
        }
      ]
    },
    {
      "name": "Set",
      "item": [
        {
          "id": "aa5951f1-2c68-4fee-9d73-b5b6e07cef5f",
          "name": "postMembersSetPermissions",
          "request": {
            "url": "http://api.dropbox.com/1/team/members/set_permissions?external_id=%7B%7D&member_id=%7B%7D&new_is_admin=%7B%7D",
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "Set member permissions."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "22e23892-a43f-4cfd-bc69-5f1b81371845"
            }
          ]
        },
        {
          "id": "1dd63b8d-8f17-4e5b-94f5-45d7d5435968",
          "name": "getMembersSetProfile",
          "request": {
            "url": "http://api.dropbox.com/1/team/members/set_profile?external_id=%7B%7D&member_id=%7B%7D&new_email=%7B%7D&new_external_id=%7B%7D&new_given_name=%7B%7D&new_surname=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Set profile."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e7c2f95a-c1aa-4119-8025-763c86e338ba"
            }
          ]
        }
      ]
    },
    {
      "name": "Activity",
      "item": [
        {
          "id": "c48634e7-1e33-43d6-936b-f9f42f961231",
          "name": "postReportsGetActivity",
          "request": {
            "url": "http://api.dropbox.com/1/team/reports/get_activity?end_date=%7B%7D&start_date=%7B%7D",
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "Get activity."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b2b35211-ec04-40bc-8978-9c954457580d"
            }
          ]
        }
      ]
    }
  ]
}