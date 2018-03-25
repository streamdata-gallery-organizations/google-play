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
  /turnbasedmatches/{matchId}/leaveTurn:
    put:
      summary: ReLeave Turnturn Turn-Based Match
      description: Leave a turn-based match during the current player's turn, without
        canceling the match
      operationId: games.turnBasedMatches.leaveTurn
      parameters:
      - in: query
        name: consistencyToken
        description: The last-seen mutation timestamp
      - in: query
        name: language
        description: The preferred language to use for strings returned by this method
      - in: path
        name: matchId
        description: The ID of the match
      - in: query
        name: matchVersion
        description: The version of the match being updated
      - in: query
        name: pendingParticipantId
        description: The ID of another participant who should take their turn next
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