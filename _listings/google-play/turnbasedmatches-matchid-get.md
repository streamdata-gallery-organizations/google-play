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
  /turnbasedmatches/{matchId}:
    get:
      summary: Get Turn-Based Match
      description: Get the data for a turn-based match
      operationId: games.turnBasedMatches.get
      parameters:
      - in: query
        name: consistencyToken
        description: The last-seen mutation timestamp
      - in: query
        name: includeMatchData
        description: Get match data along with metadata
      - in: query
        name: language
        description: The preferred language to use for strings returned by this method
      - in: path
        name: matchId
        description: The ID of the match
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