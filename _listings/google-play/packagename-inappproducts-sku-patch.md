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
    patch:
      summary: Update In App Product
      description: Updates the details of an in-app product
      operationId: androidpublisher.inappproducts.patch
      parameters:
      - in: query
        name: autoConvertMissingPrices
        description: If true the prices for all regions targeted by the parent app
          that don't have a price specified for this in-app product will be auto converted
          to the target currency based on the default price
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: packageName
        description: Unique identifier for the Android app with the in-app product;
          for example, "com
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