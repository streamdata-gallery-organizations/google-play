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
  /{packageName}/edits/{editId}/apks/{apkVersionCode}/listings/{language}:
    put:
      summary: Update APK Localized Listing
      description: Updates or creates the APK-specific localized listing for a specified
        APK and language code
      operationId: androidpublisher.edits.apklistings.update
      parameters:
      - in: path
        name: apkVersionCode
        description: The APK version code whose APK-specific listings should be read
          or modified
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: editId
        description: Unique identifier for this edit
      - in: path
        name: language
        description: The language code (a BCP-47 language tag) of the APK-specific
          localized listing to read or modify
      - in: path
        name: packageName
        description: Unique identifier for the Android app that is being updated;
          for example, "com
      responses:
        200:
          description: OK
      tags:
      - apk localized listing
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