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
  /enterprises/{enterpriseId}/users/{userId}/entitlements/{entitlementId}:
    patch:
      summary: Update Entitlement
      description: Adds or updates an entitlement to an app for a user
      operationId: androidenterprise.entitlements.patch
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: enterpriseId
        description: The ID of the enterprise
      - in: path
        name: entitlementId
        description: The ID of the entitlement (a product ID), e
      - in: query
        name: install
        description: Set to true to also install the product on all the user's devices
          where possible
      - in: path
        name: userId
        description: The ID of the user
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