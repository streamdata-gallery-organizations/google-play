---
swagger: "2.0"
info:
  title: Google Play
  version: 1.0.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /enterprises/signupUrl:
    post:
      summary: ""
      description: Generates a sign-up URL
      operationId: androidenterprise.enterprises.generateSignupUrl
      parameters:
      - in: query
        name: callbackUrl
        description: The callback URL to which the Admin will be redirected after
          successfully creating an enterprise
      responses:
        200:
          description: OK
      tags:
      - signup
definitions: []
x-collection-name: Google Play
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