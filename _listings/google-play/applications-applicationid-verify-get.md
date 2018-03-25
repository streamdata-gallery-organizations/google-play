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
  /applications/{applicationId}/verify:
    get:
      summary: Verify Token
      description: Verifies the auth token provided with this request is for the application
        with the specified ID, and returns the ID of the player it was granted for
      operationId: games.applications.verify
      parameters:
      - in: path
        name: applicationId
        description: The application ID from the Google Play developer console
      - in: query
        name: consistencyToken
        description: The last-seen mutation timestamp
      responses:
        200:
          description: OK
      tags:
      - token
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