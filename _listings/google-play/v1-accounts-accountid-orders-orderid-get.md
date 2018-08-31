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
  /v1/accounts/{accountId}/orders/{orderId}:
    get:
      summary: Get Order
      description: Get an Order given its id
      operationId: playmoviespartner.accounts.orders.get
      parameters:
      - in: path
        name: accountId
        description: REQUIRED
      - in: path
        name: orderId
        description: REQUIRED
      responses:
        200:
          description: OK
      tags:
      - order
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