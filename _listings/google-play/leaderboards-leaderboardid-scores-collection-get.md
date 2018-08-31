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
  /leaderboards/{leaderboardId}/scores/{collection}:
    get:
      summary: Get Leader Board Scores
      description: Lists the scores in a leaderboard, starting from the top
      operationId: games.scores.list
      parameters:
      - in: path
        name: collection
        description: The collection of scores you're requesting
      - in: query
        name: consistencyToken
        description: The last-seen mutation timestamp
      - in: query
        name: language
        description: The preferred language to use for strings returned by this method
      - in: path
        name: leaderboardId
        description: The ID of the leaderboard
      - in: query
        name: maxResults
        description: The maximum number of leaderboard scores to return in the response
      - in: query
        name: pageToken
        description: The token returned by the previous request
      - in: query
        name: timeSpan
        description: The time span for the scores and ranks you're requesting
      responses:
        200:
          description: OK
      tags:
      - leader board
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