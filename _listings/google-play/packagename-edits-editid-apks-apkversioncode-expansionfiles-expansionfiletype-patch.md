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
  /{packageName}/edits/{editId}/apks/{apkVersionCode}/expansionFiles/{expansionFileType}:
    patch:
      summary: 'Update APK Expansion File '
      description: Updates the APK's Expansion File configuration to reference another
        APK's Expansion Files
      operationId: androidpublisher.edits.expansionfiles.patch
      parameters:
      - in: path
        name: apkVersionCode
        description: The version code of the APK whose Expansion File configuration
          is being read or modified
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: editId
        description: Unique identifier for this edit
      - in: path
        name: expansionFileType
      - in: path
        name: packageName
        description: Unique identifier for the Android app that is being updated;
          for example, "com
      responses:
        200:
          description: OK
      tags:
      - apk expansion file
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