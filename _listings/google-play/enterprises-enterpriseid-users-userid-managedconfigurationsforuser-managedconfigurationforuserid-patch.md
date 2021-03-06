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
  /enterprises/{enterpriseId}/users/{userId}/managedConfigurationsForUser/{managedConfigurationForUserId}:
    patch:
      summary: Update Per User Configuration
      description: Adds or updates a per-user managed configuration for an app for
        the specified user
      operationId: androidenterprise.managedconfigurationsforuser.patch
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: enterpriseId
        description: The ID of the enterprise
      - in: path
        name: managedConfigurationForUserId
        description: The ID of the managed configuration (a product ID), e
      - in: path
        name: userId
        description: The ID of the user
      responses:
        200:
          description: OK
      tags:
      - configuration
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