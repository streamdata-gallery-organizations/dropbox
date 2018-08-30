{
  "info": {
    "name": "Cloud Elements - Dropbox For Business API List Members",
    "_postman_id": "93cc0d64-ef51-4307-880f-80e2fea7fb2b",
    "description": "List members.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Info",
      "item": [
        {
          "id": "08c422ab-80f7-425c-9246-f65a4e7fe1fe",
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
              "id": "b435cbba-f8aa-4a9f-ab16-922e33289c6f"
            }
          ]
        },
        {
          "id": "68c43709-ac12-4edf-bf77-a66f4c3962c5",
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
              "id": "afbec612-a240-4f13-a511-bb48ceddb0a3"
            }
          ]
        }
      ]
    },
    {
      "name": "Events",
      "item": [
        {
          "id": "192cf35d-9c73-4569-8817-d9485f871918",
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
              "id": "26ee4e25-cc00-4e7d-8f66-73a85f837866"
            }
          ]
        }
      ]
    },
    {
      "name": "Member",
      "item": [
        {
          "id": "beda3b80-92b9-430d-82c6-d2687312d8cf",
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
              "id": "99e96817-2a85-46fb-bfa1-16db8d8f48a8"
            }
          ]
        },
        {
          "id": "ef1b1456-69f5-4db6-9639-80973a4b6105",
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
              "id": "a782cece-4ed1-4c4d-a32d-86af6b83dc89"
            }
          ]
        }
      ]
    },
    {
      "name": "List",
      "item": [
        {
          "id": "dff107ca-a27c-442b-904c-fbd5cd91a0e3",
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
              "id": "c9d43ece-343b-4c47-86e6-bd391cb85556"
            }
          ]
        }
      ]
    }
  ]
}