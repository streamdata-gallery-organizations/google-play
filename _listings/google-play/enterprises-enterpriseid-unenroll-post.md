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
  /enterprises/{enterpriseId}/unenroll:
    post:
      summary: Unenroll Enterprise
      description: Unenrolls an enterprise from the calling EMM
      operationId: androidenterprise.enterprises.unenroll
      parameters:
      - in: path
        name: enterpriseId
        description: The ID of the enterprise
      responses:
        200:
          description: OK
      tags:
      - enterprise
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