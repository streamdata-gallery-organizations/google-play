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
  /{packageName}/purchases/voidedpurchases:
    get:
      summary: List Cancelled Purches
      description: Lists the purchases that were cancelled, refunded or charged-back
      operationId: androidpublisher.purchases.voidedpurchases.list
      parameters:
      - in: query
        name: endTime
        description: The time, in milliseconds since the Epoch, of the newest voided
          in-app product purchase that you want to see in the response
      - in: query
        name: maxResults
      - in: path
        name: packageName
        description: The package name of the application for which voided purchases
          need to be returned (for example, 'com
      - in: query
        name: startIndex
      - in: query
        name: startTime
        description: The time, in milliseconds since the Epoch, of the oldest voided
          in-app product purchase that you want to see in the response
      - in: query
        name: token
      responses:
        200:
          description: OK
      tags:
      - subscription
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