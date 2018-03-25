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
  /enterprises/completeSignup:
    post:
      summary: Complete Signup Flow
      description: Completes the signup flow, by specifying the Completion token and
        Enterprise token
      operationId: androidenterprise.enterprises.completeSignup
      parameters:
      - in: query
        name: completionToken
        description: The Completion token initially returned by GenerateSignupUrl
      - in: query
        name: enterpriseToken
        description: The Enterprise token appended to the Callback URL
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