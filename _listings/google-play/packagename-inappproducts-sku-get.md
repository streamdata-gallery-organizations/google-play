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
  /{packageName}/inappproducts/{sku}:
    get:
      summary: Get In App Product
      description: Returns information about the in-app product specified
      operationId: androidpublisher.inappproducts.get
      parameters:
      - in: path
        name: packageName
      - in: path
        name: sku
        description: Unique identifier for the in-app product
      responses:
        200:
          description: OK
      tags:
      - in app product
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