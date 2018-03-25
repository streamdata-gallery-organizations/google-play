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
  /{packageName}/entitlements:
    get:
      summary: Get Entitlements
      description: Lists the user's current inapp item or subscription entitlements
      operationId: androidpublisher.entitlements.list
      parameters:
      - in: query
        name: maxResults
      - in: path
        name: packageName
        description: The package name of the application the inapp product was sold
          in (for example, 'com
      - in: query
        name: productId
        description: The product id of the inapp product (for example, 'sku1')
      - in: query
        name: startIndex
      - in: query
        name: token
      responses:
        200:
          description: OK
      tags:
      - entitlement
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