---
swagger: "2.0"
x-collection-name: Google Play
x-complete: 0
info:
  title: Google Play Get App Details
  version: 1.0.0
  description: Returns all of the localized store listings attached to this edit.
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
    post:
      summary: Upload APK Expansion File
      description: Uploads and attaches a new Expansion File to the APK specified.
      operationId: androidpublisher.edits.expansionfiles.upload
      x-api-path-slug: packagenameeditseditidapksapkversioncodeexpansionfilesexpansionfiletype-post
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
      - APK Expansion File
    put:
      summary: Update APK Expansion File
      description: Updates the APK's Expansion File configuration to reference another
        APK's Expansion Files. To add a new Expansion File use the Upload method.
      operationId: androidpublisher.edits.expansionfiles.update
      x-api-path-slug: packagenameeditseditidapksapkversioncodeexpansionfilesexpansionfiletype-put
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
  /{packageName}/edits/{editId}/apks/{apkVersionCode}/listings:
    delete:
      summary: Delete All APK Localized Listing
      description: Deletes all the APK-specific localized listings for a specified
        APK.
      operationId: androidpublisher.edits.apklistings.deleteall
      x-api-path-slug: packagenameeditseditidapksapkversioncodelistings-delete
      parameters:
      - in: path
        name: apkVersionCode
        description: The APK version code whose APK-specific listings should be read
          or modified
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
      - APK Localized Listing
    get:
      summary: Get APK Localized Listings
      description: Lists all the APK-specific localized listings for a specified APK.
      operationId: androidpublisher.edits.apklistings.list
      x-api-path-slug: packagenameeditseditidapksapkversioncodelistings-get
      parameters:
      - in: path
        name: apkVersionCode
        description: The APK version code whose APK-specific listings should be read
          or modified
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
      - APK Localized Listing
  /{packageName}/edits/{editId}/apks/{apkVersionCode}/listings/{language}:
    delete:
      summary: Delete APK Localized Listing
      description: Deletes the APK-specific localized listing for a specified APK
        and language code.
      operationId: androidpublisher.edits.apklistings.delete
      x-api-path-slug: packagenameeditseditidapksapkversioncodelistingslanguage-delete
      parameters:
      - in: path
        name: apkVersionCode
        description: The APK version code whose APK-specific listings should be read
          or modified
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
          for example, com
      responses:
        200:
          description: OK
      tags:
      - APK Localized Listing
    get:
      summary: Get APK Localized Listing
      description: Fetches the APK-specific localized listing for a specified APK
        and language code.
      operationId: androidpublisher.edits.apklistings.get
      x-api-path-slug: packagenameeditseditidapksapkversioncodelistingslanguage-get
      parameters:
      - in: path
        name: apkVersionCode
        description: The APK version code whose APK-specific listings should be read
          or modified
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
          for example, com
      responses:
        200:
          description: OK
      tags:
      - APK Localized Listing
    patch:
      summary: Update APK Localized Listing
      description: Updates or creates the APK-specific localized listing for a specified
        APK and language code. This method supports patch semantics.
      operationId: androidpublisher.edits.apklistings.patch
      x-api-path-slug: packagenameeditseditidapksapkversioncodelistingslanguage-patch
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
          for example, com
      responses:
        200:
          description: OK
      tags:
      - APK Localized Listing
    put:
      summary: Update APK Localized Listing
      description: Updates or creates the APK-specific localized listing for a specified
        APK and language code.
      operationId: androidpublisher.edits.apklistings.update
      x-api-path-slug: packagenameeditseditidapksapkversioncodelistingslanguage-put
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
          for example, com
      responses:
        200:
          description: OK
      tags:
      - APK Localized Listing
  /{packageName}/edits/{editId}/details:
    get:
      summary: Get App Detail
      description: Fetches app details for this edit. This includes the default language
        and developer support contact information.
      operationId: androidpublisher.edits.details.get
      x-api-path-slug: packagenameeditseditiddetails-get
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
    patch:
      summary: Update App Detail
      description: Updates app details for this edit. This method supports patch semantics.
      operationId: androidpublisher.edits.details.patch
      x-api-path-slug: packagenameeditseditiddetails-patch
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
    put:
      summary: Update App Detail
      description: Updates app details for this edit.
      operationId: androidpublisher.edits.details.update
      x-api-path-slug: packagenameeditseditiddetails-put
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
  /{packageName}/edits/{editId}/listings:
    delete:
      summary: Delete App Detail
      description: Deletes all localized listings from an edit.
      operationId: androidpublisher.edits.listings.deleteall
      x-api-path-slug: packagenameeditseditidlistings-delete
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
      summary: Get App Details
      description: Returns all of the localized store listings attached to this edit.
      operationId: androidpublisher.edits.listings.list
      x-api-path-slug: packagenameeditseditidlistings-get
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