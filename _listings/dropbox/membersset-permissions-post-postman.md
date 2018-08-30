{
  "info": {
    "name": "Cloud Elements - Dropbox For Business API Set Member Permissions",
    "_postman_id": "2f4640d2-9580-4ad0-9942-25a972db3e7e",
    "description": "Set member permissions.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Info",
      "item": [
        {
          "id": "19f2289f-e907-4108-a251-da8ab34f8fbd",
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
              "id": "f31a414a-2625-40ff-a544-caf213cce6bc"
            }
          ]
        },
        {
          "id": "15d3ddda-0f8a-4b1b-a5de-a7e21ca3b1a1",
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
              "id": "38f70fd7-a5cb-4d88-81f4-d758dc8a7863"
            }
          ]
        }
      ]
    },
    {
      "name": "Events",
      "item": [
        {
          "id": "2c2caf9b-9ff5-4ad8-a23d-2dd0ad8c54b1",
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
              "id": "4da498f0-2f4d-4daf-8d2c-e94c72429ff4"
            }
          ]
        }
      ]
    },
    {
      "name": "Member",
      "item": [
        {
          "id": "a446b20b-7797-4c11-839f-1c440a02106a",
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
              "id": "e76e9010-59ba-41a7-80cf-8ef423513eed"
            }
          ]
        },
        {
          "id": "191a5fa2-e743-4bb1-8080-1c3859409c6b",
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
              "id": "9744c49c-3e0b-4a06-a936-3982dabe18e8"
            }
          ]
        }
      ]
    },
    {
      "name": "List",
      "item": [
        {
          "id": "3f15c81e-e745-4a10-9ba8-ef04e22aed86",
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
              "id": "3ebd118b-5c91-4de2-b3c0-0242980f84a4"
            }
          ]
        }
      ]
    },
    {
      "name": "Remove",
      "item": [
        {
          "id": "de223401-93b1-4212-94f8-53b7d9f525a3",
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
              "id": "c7fefb29-f18a-4320-bd91-31987c33edcb"
            }
          ]
        }
      ]
    },
    {
      "name": "Set",
      "item": [
        {
          "id": "cbc60837-e1b9-4c2e-9b37-cf94fe3cf96c",
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
              "id": "9e5384ad-b8ba-4978-a2da-a73689567b1e"
            }
          ]
        }
      ]
    }
  ]
}