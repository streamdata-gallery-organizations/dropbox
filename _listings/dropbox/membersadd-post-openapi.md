---
swagger: "2.0"
x-collection-name: Dropbox
x-complete: 0
info:
  title: Cloud Elements - Dropbox For Business API Add Member
  description: Add member.
  version: "1"
host: api.dropbox.com
basePath: /1/team
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /get_info:
    post:
      summary: Get Info
      description: Get info.
      operationId: postGetInfo
      x-api-path-slug: get-info-post
      responses:
        200:
          description: OK
      tags:
      - Info
  /log/get_events:
    post:
      summary: Get Events
      description: Get events.
      operationId: postLogGetEvents
      x-api-path-slug: logget-events-post
      parameters:
      - in: query
        name: category
        description: optional filter the returned events to a single category (see
          Event types below)
      - in: query
        name: cursor
        description: optional encoded value indicating from what point to get the
          next limit logs
      - in: query
        name: end_ts
        description: optional end time (UTC timestamp in milliseconds since the Unix
          epoch)
      - in: query
        name: limit
        description: optional number of results to return per call (default 1000,
          maximum 1000)
      - in: query
        name: start_ts
        description: optional start time (UTC timestamp in milliseconds since the
          Unix epoch)
      - in: query
        name: user
        description: optional member ID, user ID, or email of a user for filtering
          events
      responses:
        200:
          description: OK
      tags:
      - Events
  /members/add:
    post:
      summary: Add Member
      description: Add member.
      operationId: postMembersAdd
      x-api-path-slug: membersadd-post
      parameters:
      - in: query
        name: member_email
        description: member email
      - in: query
        name: member_external_id
        description: optional external ID for member
      - in: query
        name: member_given_name
        description: member first name
      - in: query
        name: member_surname
        description: member last name
      - in: query
        name: send_welcome_email
        description: optional boolean to send a welcome email to the member
      responses:
        200:
          description: OK
      tags:
      - Member
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---