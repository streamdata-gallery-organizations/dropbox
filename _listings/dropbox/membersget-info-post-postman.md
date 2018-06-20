{
  "info": {
    "name": "Cloud Elements - Dropbox For Business API Get Member Info",
    "_postman_id": "1a3b6de4-74ca-418b-9fa8-a2cbadaae545",
    "description": "Get member info.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Info",
      "item": [
        {
          "id": "d0d5fa24-bf26-4fea-af69-65597c656954",
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
              "id": "ced23abe-69aa-4359-b61a-3ca2005ba95d"
            }
          ]
        }
      ]
    },
    {
      "name": "Events",
      "item": [
        {
          "id": "d8497c76-20c7-41de-8065-57faaf00aff8",
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
              "id": "c5b9a54f-e70c-45ec-a6d1-bd3886dde508"
            }
          ]
        }
      ]
    },
    {
      "name": "Member",
      "item": [
        {
          "id": "2dd3c120-0963-4de5-8806-d9896a64d710",
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
              "id": "2184b929-0f9e-49a1-a5d4-662b0269af92"
            }
          ]
        },
        {
          "id": "85243b73-f0f9-407f-b5cf-876061ab4828",
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
              "id": "d33bdfcd-c5cb-4abf-92c2-d5b1286b318c"
            }
          ]
        }
      ]
    }
  ]
}