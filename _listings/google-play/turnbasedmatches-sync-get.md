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
  /turnbasedmatches/sync:
    get:
      summary: Sync Turn-Based Match
      description: Returns turn-based matches the player is or was involved in that
        changed since the last sync call, with the least recent changes coming first
      operationId: games.turnBasedMatches.sync
      parameters:
      - in: query
        name: consistencyToken
        description: The last-seen mutation timestamp
      - in: query
        name: includeMatchData
        description: True if match data should be returned in the response
      - in: query
        name: language
        description: The preferred language to use for strings returned by this method
      - in: query
        name: maxCompletedMatches
        description: The maximum number of completed or canceled matches to return
          in the response
      - in: query
        name: maxResults
        description: The maximum number of matches to return in the response, used
          for paging
      - in: query
        name: pageToken
        description: The token returned by the previous request
      responses:
        200:
          description: OK
      tags:
      - match
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