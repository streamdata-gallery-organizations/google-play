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
  /achievements/{achievementId}/setStepsAtLeast:
    post:
      summary: Set Steps for Achievements
      description: Sets the steps for the currently authenticated player towards unlocking
        an achievement
      operationId: games.achievements.setStepsAtLeast
      parameters:
      - in: path
        name: achievementId
        description: The ID of the achievement used by this method
      - in: query
        name: consistencyToken
        description: The last-seen mutation timestamp
      - in: query
        name: steps
        description: The minimum value to set the steps to
      responses:
        200:
          description: OK
      tags:
      - achievement
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