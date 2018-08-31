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
  /enterprises/pullNotificationSet:
    post:
      summary: Get Notification Set
      description: Pulls and returns a notification set for the enterprises associated
        with the service account authenticated for the request
      operationId: androidenterprise.enterprises.pullNotificationSet
      parameters:
      - in: query
        name: requestMode
        description: The request mode for pulling notifications
      responses:
        200:
          description: OK
      tags:
      - notification
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