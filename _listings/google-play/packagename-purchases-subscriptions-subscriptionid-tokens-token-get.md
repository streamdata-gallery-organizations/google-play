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
  /{packageName}/purchases/subscriptions/{subscriptionId}/tokens/{token}:
    get:
      summary: Check User Subscriptions
      description: Checks whether a user's subscription purchase is valid and returns
        its expiry time
      operationId: androidpublisher.purchases.subscriptions.get
      parameters:
      - in: path
        name: packageName
        description: The package name of the application for which this subscription
          was purchased (for example, 'com
      - in: path
        name: subscriptionId
        description: The purchased subscription ID (for example, 'monthly001')
      - in: path
        name: token
        description: The token provided to the user's device when the subscription
          was purchased
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