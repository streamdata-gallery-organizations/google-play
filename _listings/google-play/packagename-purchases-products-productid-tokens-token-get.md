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
  /{packageName}/purchases/products/{productId}/tokens/{token}:
    get:
      summary: Get In App Purchases
      description: Checks the purchase and consumption status of an inapp item
      operationId: androidpublisher.purchases.products.get
      parameters:
      - in: path
        name: packageName
        description: The package name of the application the inapp product was sold
          in (for example, 'com
      - in: path
        name: productId
        description: The inapp product SKU (for example, 'com
      - in: path
        name: token
        description: The token provided to the user's device when the inapp product
          was purchased
      responses:
        200:
          description: OK
      tags:
      - in app purchase
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