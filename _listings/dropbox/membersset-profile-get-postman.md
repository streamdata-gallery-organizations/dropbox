{
  "info": {
    "name": "Cloud Elements - Dropbox For Business API Set Profile",
    "_postman_id": "f5fcea07-428e-4547-9155-1d33b5d8fc17",
    "description": "Set profile.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Info",
      "item": [
        {
          "id": "ce7c6129-61e8-4195-9a88-37140f94c050",
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
              "id": "b965da27-f071-4dcf-b26a-014e48c9d054"
            }
          ]
        },
        {
          "id": "988edaeb-f33e-4a6c-a1c3-daff4e9257e9",
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
              "id": "ac4f9666-46e6-4763-8503-58f480bbe15d"
            }
          ]
        }
      ]
    },
    {
      "name": "Events",
      "item": [
        {
          "id": "34b4dd7c-02c7-4fb5-a5a8-a37d96c4958f",
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
              "id": "fd126f47-5f3d-4ace-b1c8-8c87f70e2dc8"
            }
          ]
        }
      ]
    },
    {
      "name": "Member",
      "item": [
        {
          "id": "262b59c7-6aaa-42f9-a81e-09dcd9f61326",
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
              "id": "5545ba2b-51b1-4941-a0b6-e69a010a7440"
            }
          ]
        },
        {
          "id": "0750f4da-8173-4d54-a16a-68d5c01785fe",
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
              "id": "cf5411ab-24b1-4507-a50c-8488c277a14f"
            }
          ]
        }
      ]
    },
    {
      "name": "List",
      "item": [
        {
          "id": "948542f5-8c34-466e-8be4-4507a75c63c6",
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
              "id": "ddf663dc-87f5-453a-ae09-f7c793e2c199"
            }
          ]
        }
      ]
    },
    {
      "name": "Remove",
      "item": [
        {
          "id": "7fae6d6a-5fb6-43a0-ab5c-0ccfc835b62f",
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
              "id": "c102e4ec-8a9d-4653-bc71-da5f4dbe904b"
            }
          ]
        }
      ]
    },
    {
      "name": "Set",
      "item": [
        {
          "id": "2e4deaf0-e1a3-4c6a-aa4b-250169dc83fa",
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
              "id": "959346c4-b530-455e-a9a2-9a94bab021fb"
            }
          ]
        },
        {
          "id": "110bf9f9-0ec2-4bc9-8944-7bb5186bd8a7",
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
              "id": "564140e5-5164-4d0e-8b7e-f1a0872dba2f"
            }
          ]
        }
      ]
    }
  ]
}