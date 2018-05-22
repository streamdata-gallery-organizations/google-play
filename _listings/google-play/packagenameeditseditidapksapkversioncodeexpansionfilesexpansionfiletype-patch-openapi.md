---
swagger: "2.0"
x-collection-name: Google Play
x-complete: 0
info:
  title: Google Play Update APK Expansion File
  version: 1.0.0
  description: Updates the APK's Expansion File configuration to reference another
    APK's Expansion Files. To add a new Expansion File use the Upload method. This
    method supports patch semantics.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /{packageName}/edits:
    post:
      summary: Create App Edit
      description: Creates a new edit for an app, populated with the app's current
        state.
      operationId: androidpublisher.edits.insert
      x-api-path-slug: packagenameedits-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: packageName
        description: Unique identifier for the Android app that is being updated;
          for example, com
      responses:
        200:
          description: OK
      tags:
      - Application
  /{packageName}/edits/{editId}:
    delete:
      summary: Delete App Edit
      description: Deletes an edit for an app. Creating a new edit will automatically
        delete any of your previous edits so this method need only be called if you
        want to preemptively abandon an edit.
      operationId: androidpublisher.edits.delete
      x-api-path-slug: packagenameeditseditid-delete
      parameters:
      - in: path
        name: editId
        description: Unique identifier for this edit
      - in: path
        name: packageName
        description: Unique identifier for the Android app that is being updated;
          for example, com
      responses:
        200:
          description: OK
      tags:
      - Application
    get:
      summary: DGetelete App Edit
      description: Returns information about the edit specified. Calls will fail if
        the edit is no long active (e.g. has been deleted, superseded or expired).
      operationId: androidpublisher.edits.get
      x-api-path-slug: packagenameeditseditid-get
      parameters:
      - in: path
        name: editId
        description: Unique identifier for this edit
      - in: path
        name: packageName
        description: Unique identifier for the Android app that is being updated;
          for example, com
      responses:
        200:
          description: OK
      tags:
      - Application
  /{packageName}/edits/{editId}/apks/externallyHosted:
    post:
      summary: Create APK
      description: Creates a new APK without uploading the APK itself to Google Play,
        instead hosting the APK at a specified URL. This function is only available
        to enterprises using Google Play for Work whose application is configured
        to restrict distribution to the enterprise domain.
      operationId: androidpublisher.edits.apks.addexternallyhosted
      x-api-path-slug: packagenameeditseditidapksexternallyhosted-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: editId
        description: Unique identifier for this edit
      - in: path
        name: packageName
        description: Unique identifier for the Android app that is being updated;
          for example, com
      responses:
        200:
          description: OK
      tags:
      - Application
  /{packageName}/edits/{editId}/apks/{apkVersionCode}/deobfuscationFiles/{deobfuscationFileType}:
    post:
      summary: Update Deobfuscation FIle
      description: Uploads the deobfuscation file of the specified APK. If a deobfuscation
        file already exists, it will be replaced.
      operationId: androidpublisher.edits.deobfuscationfiles.upload
      x-api-path-slug: packagenameeditseditidapksapkversioncodedeobfuscationfilesdeobfuscationfiletype-post
      parameters:
      - in: path
        name: apkVersionCode
        description: The version code of the APK whose deobfuscation file is being
          uploaded
      - in: path
        name: deobfuscationFileType
      - in: path
        name: editId
        description: Unique identifier for this edit
      - in: path
        name: packageName
        description: Unique identifier of the Android app for which the deobfuscatiuon
          files are being uploaded; for example, com
      responses:
        200:
          description: OK
      tags:
      - Deobfuscation FIle
  /{packageName}/edits/{editId}/apks/{apkVersionCode}/expansionFiles/{expansionFileType}:
    get:
      summary: Get Expansion File
      description: Fetches the Expansion File configuration for the APK specified.
      operationId: androidpublisher.edits.expansionfiles.get
      x-api-path-slug: packagenameeditseditidapksapkversioncodeexpansionfilesexpansionfiletype-get
      parameters:
      - in: path
        name: apkVersionCode
        description: The version code of the APK whose Expansion File configuration
          is being read or modified
      - in: path
        name: editId
        description: Unique identifier for this edit
      - in: path
        name: expansionFileType
      - in: path
        name: packageName
        description: Unique identifier for the Android app that is being updated;
          for example, com
      responses:
        200:
          description: OK
      tags:
      - Expansion File
    patch:
      summary: Update APK Expansion File
      description: Updates the APK's Expansion File configuration to reference another
        APK's Expansion Files. To add a new Expansion File use the Upload method.
        This method supports patch semantics.
      operationId: androidpublisher.edits.expansionfiles.patch
      x-api-path-slug: packagenameeditseditidapksapkversioncodeexpansionfilesexpansionfiletype-patch
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
          for example, com
      responses:
        200:
          description: OK
      tags:
      - APK Expansion File
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