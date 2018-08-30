{
  "info": {
    "name": "Cloud Elements - Dropbox For Business API Get Membership",
    "_postman_id": "2bf72c85-a8ff-4969-a1ea-91fe007bf29e",
    "description": "Get membership.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Info",
      "item": [
        {
          "id": "8c18ee50-3db0-4e7c-bb4c-f424c64e4b9a",
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
              "id": "8b222f8e-d50b-4497-96bd-4574d3c0ad89"
            }
          ]
        },
        {
          "id": "d4f2ca13-68f2-47ac-907c-e3bf56c8cb2c",
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
              "id": "053f1d65-fbfb-4d6f-9054-b8fd23c5c8c1"
            }
          ]
        }
      ]
    },
    {
      "name": "Events",
      "item": [
        {
          "id": "aa7d45c9-b7cc-4988-b0b4-12692f3a01a6",
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
              "id": "10d8e4ae-52ea-4b5f-a373-96efb79c3448"
            }
          ]
        }
      ]
    },
    {
      "name": "Member",
      "item": [
        {
          "id": "6d35c550-1a1c-4616-a1f2-0b94d9b6257b",
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
              "id": "dbfdd171-879c-41a8-b288-0bdf38b88f7b"
            }
          ]
        },
        {
          "id": "60290d71-5643-47af-89fa-0fc06eb0705c",
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
              "id": "4edb04fb-40f9-492b-b7d1-a51a50744d52"
            }
          ]
        }
      ]
    },
    {
      "name": "List",
      "item": [
        {
          "id": "fbd1875f-6357-4132-afe7-23d48719e99a",
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
              "id": "021917ea-91b4-4396-b93d-45c85732140f"
            }
          ]
        }
      ]
    },
    {
      "name": "Remove",
      "item": [
        {
          "id": "f5d1c96e-4fe0-4993-8090-b76f95ba59a6",
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
              "id": "80782aa8-2fe4-411e-9bce-2f104ccd4ebf"
            }
          ]
        }
      ]
    },
    {
      "name": "Set",
      "item": [
        {
          "id": "3a635089-d7d7-44c8-bb27-e6a1dc581144",
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
              "id": "957bb58c-b81f-4272-9506-3db61f80c062"
            }
          ]
        },
        {
          "id": "f5a64922-141d-4007-9cec-41f281eaab87",
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
              "id": "80b22655-c5d1-4cca-9048-1bbfd3e42607"
            }
          ]
        }
      ]
    },
    {
      "name": "Activity",
      "item": [
        {
          "id": "7f65ea94-6ebc-40e2-a9a6-5a480501057f",
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
              "id": "23125c35-b69f-4819-b2bf-ea10aad0a239"
            }
          ]
        }
      ]
    },
    {
      "name": "Devices",
      "item": [
        {
          "id": "1afb6f36-7220-4d08-8e15-ed6803a65c66",
          "name": "postReportsGetDevices",
          "request": {
            "url": "http://api.dropbox.com/1/team/reports/get_devices?end_date=%7B%7D&start_date=%7B%7D",
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "Get devices."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a0aa1cb0-c34d-474a-a0bf-61a03c0cf6b6"
            }
          ]
        }
      ]
    },
    {
      "name": "Membership",
      "item": [
        {
          "id": "13ea7e38-d380-4c5b-a59a-5d57461260e9",
          "name": "postReportsGetMembership",
          "request": {
            "url": "http://api.dropbox.com/1/team/reports/get_membership?end_date=%7B%7D&start_date=%7B%7D",
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "Get membership."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e54835cb-dcce-458e-800c-8b1c39f8b8ec"
            }
          ]
        }
      ]
    }
  ]
}