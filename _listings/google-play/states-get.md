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
  /states:
    get:
      summary: Get State Keys
      description: Lists all the states keys, and optionally the state data
      operationId: appstate.states.list
      parameters:
      - in: query
        name: includeData
        description: Whether to include the full data in addition to the version number
      responses:
        200:
          description: OK
      tags:
      - application state
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