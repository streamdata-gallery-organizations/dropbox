---
swagger: "2.0"
x-collection-name: Dropbox
x-complete: 0
info:
  title: Dropbox Core Convert OAuth 1 token to OAuth 2 token.
  description: |-
    This endpoint should be used by apps transitioning from OAuth 1 to OAuth 2. It will return an OAuth 2 token
    for the authenticated user.
  termsOfService: https://www.dropbox.com/developers/reference/tos
  contact:
    name: Dropbox
    url: https://www.dropbox.com/developers
  version: 1.0.0
host: api.dropbox.com
basePath: /1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /oauth2/token_from_oauth1:
    post:
      summary: Convert OAuth 1 token to OAuth 2 token.
      description: |-
        This endpoint should be used by apps transitioning from OAuth 1 to OAuth 2. It will return an OAuth 2 token
        for the authenticated user.
      operationId: this-endpoint-should-be-used-by-apps-transitioning-from-oauth-1-to-oauth-2-it-will-return-an-oauth-2
      x-api-path-slug: oauth2token-from-oauth1-post
      responses:
        200:
          description: OK
      tags:
      - Storage
      - Documents
      - Oauth2
      - Token_from_oauth1
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