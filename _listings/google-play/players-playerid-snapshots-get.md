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
  /players/{playerId}/snapshots:
    get:
      summary: Get Player Snapshots
      description: Retrieves a list of snapshots created by your application for the
        player corresponding to the player ID
      operationId: games.snapshots.list
      parameters:
      - in: query
        name: consistencyToken
        description: The last-seen mutation timestamp
      - in: query
        name: language
        description: The preferred language to use for strings returned by this method
      - in: query
        name: maxResults
        description: The maximum number of snapshot resources to return in the response,
          used for paging
      - in: query
        name: pageToken
        description: The token returned by the previous request
      - in: path
        name: playerId
        description: A player ID
      responses:
        200:
          description: OK
      tags:
      - player
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