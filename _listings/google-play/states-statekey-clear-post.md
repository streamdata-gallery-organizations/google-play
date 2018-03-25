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
  /states/{stateKey}/clear:
    post:
      summary: Clear State Key
      description: Clears (sets to empty) the data for the passed key if and only
        if the passed version matches the currently stored version
      operationId: appstate.states.clear
      parameters:
      - in: query
        name: currentDataVersion
        description: The version of the data to be cleared
      - in: path
        name: stateKey
        description: The key for the data to be retrieved
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