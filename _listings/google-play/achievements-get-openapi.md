---
swagger: "2.0"
x-collection-name: Google Play
x-complete: 0
info:
  title: Google Play Get Achievements
  version: 1.0.0
  description: Lists all the achievement definitions for your application.
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
  /{packageName}/edits/{editId}/listings/{language}:
    delete:
      summary: Delete Localized Store Listing
      description: Deletes the specified localized store listing from an edit.
      operationId: androidpublisher.edits.listings.delete
      x-api-path-slug: packagenameeditseditidlistingslanguage-delete
      parameters:
      - in: path
        name: editId
        description: Unique identifier for this edit
      - in: path
        name: language
        description: The language code (a BCP-47 language tag) of the localized listing
          to read or modify
      - in: path
        name: packageName
        description: Unique identifier for the Android app that is being updated;
          for example, com
      responses:
        200:
          description: OK
      tags:
      - Localized Store Listing
    get:
      summary: Get Localized Store Listing
      description: Fetches information about a localized store listing.
      operationId: androidpublisher.edits.listings.get
      x-api-path-slug: packagenameeditseditidlistingslanguage-get
      parameters:
      - in: path
        name: editId
        description: Unique identifier for this edit
      - in: path
        name: language
        description: The language code (a BCP-47 language tag) of the localized listing
          to read or modify
      - in: path
        name: packageName
        description: Unique identifier for the Android app that is being updated;
          for example, com
      responses:
        200:
          description: OK
      tags:
      - Localized Store Listing
    patch:
      summary: Update Localized Store Listing
      description: Creates or updates a localized store listing. This method supports
        patch semantics.
      operationId: androidpublisher.edits.listings.patch
      x-api-path-slug: packagenameeditseditidlistingslanguage-patch
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: editId
        description: Unique identifier for this edit
      - in: path
        name: language
        description: The language code (a BCP-47 language tag) of the localized listing
          to read or modify
      - in: path
        name: packageName
        description: Unique identifier for the Android app that is being updated;
          for example, com
      responses:
        200:
          description: OK
      tags:
      - Localized Store Listing
    put:
      summary: Update Localized Store Listing
      description: Creates or updates a localized store listing.
      operationId: androidpublisher.edits.listings.update
      x-api-path-slug: packagenameeditseditidlistingslanguage-put
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: editId
        description: Unique identifier for this edit
      - in: path
        name: language
        description: The language code (a BCP-47 language tag) of the localized listing
          to read or modify
      - in: path
        name: packageName
        description: Unique identifier for the Android app that is being updated;
          for example, com
      responses:
        200:
          description: OK
      tags:
      - Localized Store Listing
  /{packageName}/edits/{editId}/listings/{language}/{imageType}:
    delete:
      summary: Delete All Images
      description: Deletes all images for the specified language and image type.
      operationId: androidpublisher.edits.images.deleteall
      x-api-path-slug: packagenameeditseditidlistingslanguageimagetype-delete
      parameters:
      - in: path
        name: editId
        description: Unique identifier for this edit
      - in: path
        name: imageType
      - in: path
        name: language
        description: The language code (a BCP-47 language tag) of the localized listing
          whose images are to read or modified
      - in: path
        name: packageName
        description: Unique identifier for the Android app that is being updated;
          for example, com
      responses:
        200:
          description: OK
      tags:
      - Image
    get:
      summary: Get All Images
      description: Lists all images for the specified language and image type.
      operationId: androidpublisher.edits.images.list
      x-api-path-slug: packagenameeditseditidlistingslanguageimagetype-get
      parameters:
      - in: path
        name: editId
        description: Unique identifier for this edit
      - in: path
        name: imageType
      - in: path
        name: language
        description: The language code (a BCP-47 language tag) of the localized listing
          whose images are to read or modified
      - in: path
        name: packageName
        description: Unique identifier for the Android app that is being updated;
          for example, com
      responses:
        200:
          description: OK
      tags:
      - Image
    post:
      summary: Upoads Image
      description: Uploads a new image and adds it to the list of images for the specified
        language and image type.
      operationId: androidpublisher.edits.images.upload
      x-api-path-slug: packagenameeditseditidlistingslanguageimagetype-post
      parameters:
      - in: path
        name: editId
        description: Unique identifier for this edit
      - in: path
        name: imageType
      - in: path
        name: language
        description: The language code (a BCP-47 language tag) of the localized listing
          whose images are to read or modified
      - in: path
        name: packageName
        description: Unique identifier for the Android app that is being updated;
          for example, com
      responses:
        200:
          description: OK
      tags:
      - Image
  /enterprises:
    get:
      summary: Get Enterprises
      description: Looks up an enterprise by domain name. This is only supported for
        enterprises created via the Google-initiated creation flow. Lookup of the
        id is not needed for enterprises created via the EMM-initiated flow since
        the EMM learns the enterprise ID in the callback specified in the Enterprises.generateSignupUrl
        call.
      operationId: androidenterprise.enterprises.list
      x-api-path-slug: enterprises-get
      parameters:
      - in: query
        name: domain
        description: The exact primary domain name of the enterprise to look up
      responses:
        200:
          description: OK
      tags:
      - Enterprise
    post:
      summary: Create Enterprise
      description: Establishes the binding between the EMM and an enterprise. This
        is now deprecated; use enroll instead.
      operationId: androidenterprise.enterprises.insert
      x-api-path-slug: enterprises-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: token
        description: The token provided by the enterprise to register the EMM
      responses:
        200:
          description: OK
      tags:
      - Enterprise
  /enterprises/acknowledgeNotificationSet:
    post:
      summary: Create Acknowledges Notification Set
      description: Acknowledges notifications that were received from Enterprises.PullNotificationSet
        to prevent subsequent calls from returning the same notifications.
      operationId: androidenterprise.enterprises.acknowledgeNotificationSet
      x-api-path-slug: enterprisesacknowledgenotificationset-post
      parameters:
      - in: query
        name: notificationSetId
        description: The notification set ID as returned by Enterprises
      responses:
        200:
          description: OK
      tags:
      - Notification
  /enterprises/completeSignup:
    post:
      summary: Complete Signup Flow
      description: Completes the signup flow, by specifying the Completion token and
        Enterprise token. This request must not be called multiple times for a given
        Enterprise Token.
      operationId: androidenterprise.enterprises.completeSignup
      x-api-path-slug: enterprisescompletesignup-post
      parameters:
      - in: query
        name: completionToken
        description: The Completion token initially returned by GenerateSignupUrl
      - in: query
        name: enterpriseToken
        description: The Enterprise token appended to the Callback URL
      responses:
        200:
          description: OK
      tags:
      - Signup
  /{packageName}/edits/{editId}/listings/{language}/{imageType}/{imageId}:
    delete:
      summary: Delete Image
      description: Deletes the image (specified by id) from the edit.
      operationId: androidpublisher.edits.images.delete
      x-api-path-slug: packagenameeditseditidlistingslanguageimagetypeimageid-delete
      parameters:
      - in: path
        name: editId
        description: Unique identifier for this edit
      - in: path
        name: imageId
        description: Unique identifier an image within the set of images attached
          to this edit
      - in: path
        name: imageType
      - in: path
        name: language
        description: The language code (a BCP-47 language tag) of the localized listing
          whose images are to read or modified
      - in: path
        name: packageName
        description: Unique identifier for the Android app that is being updated;
          for example, com
      responses:
        200:
          description: OK
      tags:
      - Image
  /enterprises/enroll:
    post:
      summary: Entroll Enterprise
      description: Enrolls an enterprise with the calling EMM.
      operationId: androidenterprise.enterprises.enroll
      x-api-path-slug: enterprisesenroll-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: token
        description: The token provided by the enterprise to register the EMM
      responses:
        200:
          description: OK
      tags:
      - Enroll
  /enterprises/pullNotificationSet:
    post:
      summary: Get Notification Set
      description: |-
        Pulls and returns a notification set for the enterprises associated with the service account authenticated for the request. The notification set may be empty if no notification are pending.
        A notification set returned needs to be acknowledged within 20 seconds by calling Enterprises.AcknowledgeNotificationSet, unless the notification set is empty.
        Notifications that are not acknowledged within the 20 seconds will eventually be included again in the response to another PullNotificationSet request, and those that are never acknowledged will ultimately be deleted according to the Google Cloud Platform Pub/Sub system policy.
        Multiple requests might be performed concurrently to retrieve notifications, in which case the pending notifications (if any) will be split among each caller, if any are pending.
        If no notifications are present, an empty notification list is returned. Subsequent requests may return more notifications once they become available.
      operationId: androidenterprise.enterprises.pullNotificationSet
      x-api-path-slug: enterprisespullnotificationset-post
      parameters:
      - in: query
        name: requestMode
        description: The request mode for pulling notifications
      responses:
        200:
          description: OK
      tags:
      - Notification
  /enterprises/signupUrl:
    post:
      summary: ""
      description: Generates a sign-up URL.
      operationId: androidenterprise.enterprises.generateSignupUrl
      x-api-path-slug: enterprisessignupurl-post
      parameters:
      - in: query
        name: callbackUrl
        description: The callback URL to which the Admin will be redirected after
          successfully creating an enterprise
      responses:
        200:
          description: OK
      tags:
      - Signup
  /enterprises/{enterpriseId}:
    delete:
      summary: Delete Enterprise
      description: Deletes the binding between the EMM and enterprise. This is now
        deprecated. Use this method only to unenroll customers that were previously
        enrolled with the insert call, then enroll them again with the enroll call.
      operationId: androidenterprise.enterprises.delete
      x-api-path-slug: enterprisesenterpriseid-delete
      parameters:
      - in: path
        name: enterpriseId
        description: The ID of the enterprise
      responses:
        200:
          description: OK
      tags:
      - Enterprise
    get:
      summary: Get Enterprise
      description: Retrieves the name and domain of an enterprise.
      operationId: androidenterprise.enterprises.get
      x-api-path-slug: enterprisesenterpriseid-get
      parameters:
      - in: path
        name: enterpriseId
        description: The ID of the enterprise
      responses:
        200:
          description: OK
      tags:
      - Enterprise
  /enterprises/{enterpriseId}/account:
    put:
      summary: Update Enterprise Account
      description: Sets the account that will be used to authenticate to the API as
        the enterprise.
      operationId: androidenterprise.enterprises.setAccount
      x-api-path-slug: enterprisesenterpriseidaccount-put
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: enterpriseId
        description: The ID of the enterprise
      responses:
        200:
          description: OK
      tags:
      - Enterprise
  /enterprises/{enterpriseId}/createWebToken:
    post:
      summary: Create Web Token
      description: Returns a unique token to access an embeddable UI. To generate
        a web UI, pass the generated token into the managed Google Play javascript
        API. Each token may only be used to start one UI session. See the javascript
        API documentation for further information.
      operationId: androidenterprise.enterprises.createWebToken
      x-api-path-slug: enterprisesenterpriseidcreatewebtoken-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: enterpriseId
        description: The ID of the enterprise
      responses:
        200:
          description: OK
      tags:
      - Token
  /enterprises/{enterpriseId}/groupLicenses:
    get:
      summary: Get Group Licenses
      description: Retrieves IDs of all products for which the enterprise has a group
        license.
      operationId: androidenterprise.grouplicenses.list
      x-api-path-slug: enterprisesenterpriseidgrouplicenses-get
      parameters:
      - in: path
        name: enterpriseId
        description: The ID of the enterprise
      responses:
        200:
          description: OK
      tags:
      - License
  /enterprises/{enterpriseId}/groupLicenses/{groupLicenseId}:
    get:
      summary: Get Group License
      description: Retrieves details of an enterprise's group license for a product.
      operationId: androidenterprise.grouplicenses.get
      x-api-path-slug: enterprisesenterpriseidgrouplicensesgrouplicenseid-get
      parameters:
      - in: path
        name: enterpriseId
        description: The ID of the enterprise
      - in: path
        name: groupLicenseId
        description: The ID of the product the group license is for, e
      responses:
        200:
          description: OK
      tags:
      - License
  /{packageName}/edits/{editId}/tracks:
    get:
      summary: Get Track Configurations
      description: Lists all the track configurations for this edit.
      operationId: androidpublisher.edits.tracks.list
      x-api-path-slug: packagenameeditseditidtracks-get
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
      - Track Configuration
  /enterprises/{enterpriseId}/groupLicenses/{groupLicenseId}/users:
    get:
      summary: Get Group License User
      description: Retrieves the IDs of the users who have been granted entitlements
        under the license.
      operationId: androidenterprise.grouplicenseusers.list
      x-api-path-slug: enterprisesenterpriseidgrouplicensesgrouplicenseidusers-get
      parameters:
      - in: path
        name: enterpriseId
        description: The ID of the enterprise
      - in: path
        name: groupLicenseId
        description: The ID of the product the group license is for, e
      responses:
        200:
          description: OK
      tags:
      - License
  /{packageName}/edits/{editId}/tracks/{track}:
    get:
      summary: Get Track Configuration
      description: Fetches the track configuration for the specified track type. Includes
        the APK version codes that are in this track.
      operationId: androidpublisher.edits.tracks.get
      x-api-path-slug: packagenameeditseditidtrackstrack-get
      parameters:
      - in: path
        name: editId
        description: Unique identifier for this edit
      - in: path
        name: packageName
        description: Unique identifier for the Android app that is being updated;
          for example, com
      - in: path
        name: track
        description: The track type to read or modify
      responses:
        200:
          description: OK
      tags:
      - Track Configuration
    patch:
      summary: Update Track Configuration
      description: Updates the track configuration for the specified track type. When
        halted, the rollout track cannot be updated without adding new APKs, and adding
        new APKs will cause it to resume. This method supports patch semantics.
      operationId: androidpublisher.edits.tracks.patch
      x-api-path-slug: packagenameeditseditidtrackstrack-patch
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
      - in: path
        name: track
        description: The track type to read or modify
      responses:
        200:
          description: OK
      tags:
      - Track Configuration
    put:
      summary: Update Track Configuration
      description: Updates the track configuration for the specified track type. When
        halted, the rollout track cannot be updated without adding new APKs, and adding
        new APKs will cause it to resume.
      operationId: androidpublisher.edits.tracks.update
      x-api-path-slug: packagenameeditseditidtrackstrack-put
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
      - in: path
        name: track
        description: The track type to read or modify
      responses:
        200:
          description: OK
      tags:
      - Track Configuration
  /enterprises/{enterpriseId}/products:
    get:
      summary: Get Products
      description: Finds approved products that match a query, or all approved products
        if there is no query.
      operationId: androidenterprise.products.list
      x-api-path-slug: enterprisesenterpriseidproducts-get
      parameters:
      - in: query
        name: approved
        description: Specifies whether to search among all products (false) or among
          only products that have been approved (true)
      - in: path
        name: enterpriseId
        description: The ID of the enterprise
      - in: query
        name: language
        description: The BCP47 tag for the users preferred language (e
      - in: query
        name: maxResults
        description: Specifies the maximum number of products that can be returned
          per request
      - in: query
        name: query
        description: The search query as typed in the Google Play store search box
      - in: query
        name: token
        description: A pagination token is contained in a requests response when there
          are more products
      responses:
        200:
          description: OK
      tags:
      - Product
  /enterprises/{enterpriseId}/products/{productId}:
    get:
      summary: Get Product
      description: Retrieves details of a product for display to an enterprise admin.
      operationId: androidenterprise.products.get
      x-api-path-slug: enterprisesenterpriseidproductsproductid-get
      parameters:
      - in: path
        name: enterpriseId
        description: The ID of the enterprise
      - in: query
        name: language
        description: The BCP47 tag for the users preferred language (e
      - in: path
        name: productId
        description: The ID of the product, e
      responses:
        200:
          description: OK
      tags:
      - Product
  /enterprises/{enterpriseId}/products/{productId}/appRestrictionsSchema:
    get:
      summary: Get Restriction Schema
      description: Retrieves the schema that defines the configurable properties for
        this product. All products have a schema, but this schema may be empty if
        no managed configurations have been defined. This schema can be used to populate
        a UI that allows an admin to configure the product. To apply a managed configuration
        based on the schema obtained using this API, see Managed Configurations through
        Play.
      operationId: androidenterprise.products.getAppRestrictionsSchema
      x-api-path-slug: enterprisesenterpriseidproductsproductidapprestrictionsschema-get
      parameters:
      - in: path
        name: enterpriseId
        description: The ID of the enterprise
      - in: query
        name: language
        description: The BCP47 tag for the users preferred language (e
      - in: path
        name: productId
        description: The ID of the product
      responses:
        200:
          description: OK
      tags:
      - Schema
  /{packageName}/edits/{editId}:commit:
    post:
      summary: Commit Changes
      description: Commits/applies the changes made in this edit back to the app.
      operationId: androidpublisher.edits.commit
      x-api-path-slug: packagenameeditseditidcommit-post
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
      - Change
  /{packageName}/edits/{editId}:validate:
    post:
      summary: Validate Changes
      description: Checks that the edit can be successfully committed. The edit's
        changes are not applied to the live app.
      operationId: androidpublisher.edits.validate
      x-api-path-slug: packagenameeditseditidvalidate-post
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
      - Change
  /enterprises/{enterpriseId}/products/{productId}/approve:
    post:
      summary: Approve Product
      description: |-
        Approves the specified product and the relevant app permissions, if any. The maximum number of products that you can approve per enterprise customer is 1,000.

        To learn how to use managed Google Play to design and create a store layout to display approved products to your users, see Store Layout Design.
      operationId: androidenterprise.products.approve
      x-api-path-slug: enterprisesenterpriseidproductsproductidapprove-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: enterpriseId
        description: The ID of the enterprise
      - in: path
        name: productId
        description: The ID of the product
      responses:
        200:
          description: OK
      tags:
      - Product
  /{packageName}/entitlements:
    get:
      summary: Get Entitlements
      description: Lists the user's current inapp item or subscription entitlements
      operationId: androidpublisher.entitlements.list
      x-api-path-slug: packagenameentitlements-get
      parameters:
      - in: query
        name: maxResults
      - in: path
        name: packageName
        description: The package name of the application the inapp product was sold
          in (for example, com
      - in: query
        name: productId
        description: The product id of the inapp product (for example, sku1)
      - in: query
        name: startIndex
      - in: query
        name: token
      responses:
        200:
          description: OK
      tags:
      - Entitlement
  /enterprises/{enterpriseId}/products/{productId}/generateApprovalUrl:
    post:
      summary: Generates a URL
      description: |-
        Generates a URL that can be rendered in an iframe to display the permissions (if any) of a product. An enterprise admin must view these permissions and accept them on behalf of their organization in order to approve that product.

        Admins should accept the displayed permissions by interacting with a separate UI element in the EMM console, which in turn should trigger the use of this URL as the approvalUrlInfo.approvalUrl property in a Products.approve call to approve the product. This URL can only be used to display permissions for up to 1 day.
      operationId: androidenterprise.products.generateApprovalUrl
      x-api-path-slug: enterprisesenterpriseidproductsproductidgenerateapprovalurl-post
      parameters:
      - in: path
        name: enterpriseId
        description: The ID of the enterprise
      - in: query
        name: languageCode
        description: The BCP 47 language code used for permission names and descriptions
          in the returned iframe, for instance en-US
      - in: path
        name: productId
        description: The ID of the product
      responses:
        200:
          description: OK
      tags:
      - URL
  /enterprises/{enterpriseId}/products/{productId}/permissions:
    get:
      summary: Retrieves the Android App Permission
      description: Retrieves the Android app permissions required by this app.
      operationId: androidenterprise.products.getPermissions
      x-api-path-slug: enterprisesenterpriseidproductsproductidpermissions-get
      parameters:
      - in: path
        name: enterpriseId
        description: The ID of the enterprise
      - in: path
        name: productId
        description: The ID of the product
      responses:
        200:
          description: OK
      tags:
      - Permission
  /{packageName}/inappproducts:
    get:
      summary: Get In App Products
      description: List all the in-app products for an Android app, both subscriptions
        and managed in-app products..
      operationId: androidpublisher.inappproducts.list
      x-api-path-slug: packagenameinappproducts-get
      parameters:
      - in: query
        name: maxResults
      - in: path
        name: packageName
        description: Unique identifier for the Android app with in-app products; for
          example, com
      - in: query
        name: startIndex
      - in: query
        name: token
      responses:
        200:
          description: OK
      tags:
      - In App Product
    post:
      summary: Create In App Products
      description: Creates a new in-app product for an app.
      operationId: androidpublisher.inappproducts.insert
      x-api-path-slug: packagenameinappproducts-post
      parameters:
      - in: query
        name: autoConvertMissingPrices
        description: If true the prices for all regions targeted by the parent app
          that dont have a price specified for this in-app product will be auto converted
          to the target currency based on the default price
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: packageName
        description: Unique identifier for the Android app; for example, com
      responses:
        200:
          description: OK
      tags:
      - In App Product
  /enterprises/{enterpriseId}/products/{productId}/unapprove:
    post:
      summary: Unnarove Product
      description: Unapproves the specified product (and the relevant app permissions,
        if any)
      operationId: androidenterprise.products.unapprove
      x-api-path-slug: enterprisesenterpriseidproductsproductidunapprove-post
      parameters:
      - in: path
        name: enterpriseId
        description: The ID of the enterprise
      - in: path
        name: productId
        description: The ID of the product
      responses:
        200:
          description: OK
      tags:
      - Product
  /enterprises/{enterpriseId}/sendTestPushNotification:
    post:
      summary: Send Test Push
      description: Sends a test push notification to validate the EMM integration
        with the Google Cloud Pub/Sub service for this enterprise.
      operationId: androidenterprise.enterprises.sendTestPushNotification
      x-api-path-slug: enterprisesenterpriseidsendtestpushnotification-post
      parameters:
      - in: path
        name: enterpriseId
        description: The ID of the enterprise
      responses:
        200:
          description: OK
      tags:
      - Testing
  /enterprises/{enterpriseId}/serviceAccount:
    get:
      summary: Return Service Account
      description: |-
        Returns a service account and credentials. The service account can be bound to the enterprise by calling setAccount. The service account is unique to this enterprise and EMM, and will be deleted if the enterprise is unbound. The credentials contain private key data and are not stored server-side.

        This method can only be called after calling Enterprises.Enroll or Enterprises.CompleteSignup, and before Enterprises.SetAccount; at other times it will return an error.

        Subsequent calls after the first will generate a new, unique set of credentials, and invalidate the previously generated credentials.

        Once the service account is bound to the enterprise, it can be managed using the serviceAccountKeys resource.
      operationId: androidenterprise.enterprises.getServiceAccount
      x-api-path-slug: enterprisesenterpriseidserviceaccount-get
      parameters:
      - in: path
        name: enterpriseId
        description: The ID of the enterprise
      - in: query
        name: keyType
        description: The type of credential to return with the service account
      responses:
        200:
          description: OK
      tags:
      - Account
  /{packageName}/inappproducts/{sku}:
    delete:
      summary: Delete In App Products
      description: Delete an in-app product for an app.
      operationId: androidpublisher.inappproducts.delete
      x-api-path-slug: packagenameinappproductssku-delete
      parameters:
      - in: path
        name: packageName
        description: Unique identifier for the Android app with the in-app product;
          for example, com
      - in: path
        name: sku
        description: Unique identifier for the in-app product
      responses:
        200:
          description: OK
      tags:
      - In App Product
    get:
      summary: Get In App Product
      description: Returns information about the in-app product specified.
      operationId: androidpublisher.inappproducts.get
      x-api-path-slug: packagenameinappproductssku-get
      parameters:
      - in: path
        name: packageName
      - in: path
        name: sku
        description: Unique identifier for the in-app product
      responses:
        200:
          description: OK
      tags:
      - In App Product
    patch:
      summary: Update In App Product
      description: Updates the details of an in-app product. This method supports
        patch semantics.
      operationId: androidpublisher.inappproducts.patch
      x-api-path-slug: packagenameinappproductssku-patch
      parameters:
      - in: query
        name: autoConvertMissingPrices
        description: If true the prices for all regions targeted by the parent app
          that dont have a price specified for this in-app product will be auto converted
          to the target currency based on the default price
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: packageName
        description: Unique identifier for the Android app with the in-app product;
          for example, com
      - in: path
        name: sku
        description: Unique identifier for the in-app product
      responses:
        200:
          description: OK
      tags:
      - In App Product
    put:
      summary: Update In App Product
      description: Updates the details of an in-app product.
      operationId: androidpublisher.inappproducts.update
      x-api-path-slug: packagenameinappproductssku-put
      parameters:
      - in: query
        name: autoConvertMissingPrices
        description: If true the prices for all regions targeted by the parent app
          that dont have a price specified for this in-app product will be auto converted
          to the target currency based on the default price
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: packageName
        description: Unique identifier for the Android app with the in-app product;
          for example, com
      - in: path
        name: sku
        description: Unique identifier for the in-app product
      responses:
        200:
          description: OK
      tags:
      - In App Product
  /enterprises/{enterpriseId}/serviceAccountKeys:
    get:
      summary: Return Active Credentials
      description: Lists all active credentials for the service account associated
        with this enterprise. Only the ID and key type are returned. The calling service
        account must have been retrieved by calling Enterprises.GetServiceAccount
        and must have been set as the enterprise service account by calling Enterprises.SetAccount.
      operationId: androidenterprise.serviceaccountkeys.list
      x-api-path-slug: enterprisesenterpriseidserviceaccountkeys-get
      parameters:
      - in: path
        name: enterpriseId
        description: The ID of the enterprise
      responses:
        200:
          description: OK
      tags:
      - Credential
    post:
      summary: Generate New Credentials
      description: |-
        Generates new credentials for the service account associated with this enterprise. The calling service account must have been retrieved by calling Enterprises.GetServiceAccount and must have been set as the enterprise service account by calling Enterprises.SetAccount.

        Only the type of the key should be populated in the resource to be inserted.
      operationId: androidenterprise.serviceaccountkeys.insert
      x-api-path-slug: enterprisesenterpriseidserviceaccountkeys-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: enterpriseId
        description: The ID of the enterprise
      responses:
        200:
          description: OK
      tags:
      - Credential
  /enterprises/{enterpriseId}/serviceAccountKeys/{keyId}:
    delete:
      summary: Remove and Invalidates Credentials
      description: Removes and invalidates the specified credentials for the service
        account associated with this enterprise. The calling service account must
        have been retrieved by calling Enterprises.GetServiceAccount and must have
        been set as the enterprise service account by calling Enterprises.SetAccount.
      operationId: androidenterprise.serviceaccountkeys.delete
      x-api-path-slug: enterprisesenterpriseidserviceaccountkeyskeyid-delete
      parameters:
      - in: path
        name: enterpriseId
        description: The ID of the enterprise
      - in: path
        name: keyId
        description: The ID of the key
      responses:
        200:
          description: OK
      tags:
      - Credential
  /enterprises/{enterpriseId}/storeLayout:
    get:
      summary: Get Store Layout
      description: Returns the store layout for the enterprise. If the store layout
        has not been set, or if the store layout has no homepageId set, returns a
        NOT_FOUND error.
      operationId: androidenterprise.enterprises.getStoreLayout
      x-api-path-slug: enterprisesenterpriseidstorelayout-get
      parameters:
      - in: path
        name: enterpriseId
        description: The ID of the enterprise
      responses:
        200:
          description: OK
      tags:
      - Store Layout
    put:
      summary: Update Store Layout
      description: Sets the store layout for the enterprise. By default, storeLayoutType
        is set to "basic" and the basic store layout is enabled. The basic layout
        only contains apps approved by the admin, and that have been added to the
        available product set for a user (using the  setAvailableProductSet call).
        Apps on the page are sorted in order of their product ID value. If you create
        a custom store layout (by setting storeLayoutType = "custom"), the basic store
        layout is disabled.
      operationId: androidenterprise.enterprises.setStoreLayout
      x-api-path-slug: enterprisesenterpriseidstorelayout-put
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: enterpriseId
        description: The ID of the enterprise
      responses:
        200:
          description: OK
      tags:
      - Store Layout
  /enterprises/{enterpriseId}/storeLayout/pages:
    get:
      summary: Get Store Layout Pages
      description: Retrieves the details of all pages in the store.
      operationId: androidenterprise.storelayoutpages.list
      x-api-path-slug: enterprisesenterpriseidstorelayoutpages-get
      parameters:
      - in: path
        name: enterpriseId
        description: The ID of the enterprise
      responses:
        200:
          description: OK
      tags:
      - Store Layout Page
    post:
      summary: Create Store Layout Page
      description: Inserts a new store page.
      operationId: androidenterprise.storelayoutpages.insert
      x-api-path-slug: enterprisesenterpriseidstorelayoutpages-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: enterpriseId
        description: The ID of the enterprise
      responses:
        200:
          description: OK
      tags:
      - Store Layout Page
  /{packageName}/purchases/products/{productId}/tokens/{token}:
    get:
      summary: Get In App Purchases
      description: Checks the purchase and consumption status of an inapp item.
      operationId: androidpublisher.purchases.products.get
      x-api-path-slug: packagenamepurchasesproductsproductidtokenstoken-get
      parameters:
      - in: path
        name: packageName
        description: The package name of the application the inapp product was sold
          in (for example, com
      - in: path
        name: productId
        description: The inapp product SKU (for example, com
      - in: path
        name: token
        description: The token provided to the users device when the inapp product
          was purchased
      responses:
        200:
          description: OK
      tags:
      - In App Purchase
  /enterprises/{enterpriseId}/storeLayout/pages/{pageId}:
    delete:
      summary: Delete Store Layout Page
      description: Deletes a store page.
      operationId: androidenterprise.storelayoutpages.delete
      x-api-path-slug: enterprisesenterpriseidstorelayoutpagespageid-delete
      parameters:
      - in: path
        name: enterpriseId
        description: The ID of the enterprise
      - in: path
        name: pageId
        description: The ID of the page
      responses:
        200:
          description: OK
      tags:
      - Store Layout Page
    get:
      summary: Get Store Layout Page
      description: Retrieves details of a store page.
      operationId: androidenterprise.storelayoutpages.get
      x-api-path-slug: enterprisesenterpriseidstorelayoutpagespageid-get
      parameters:
      - in: path
        name: enterpriseId
        description: The ID of the enterprise
      - in: path
        name: pageId
        description: The ID of the page
      responses:
        200:
          description: OK
      tags:
      - Store Layout Page
    patch:
      summary: Update Store Layout Page
      description: Updates the content of a store page. This method supports patch
        semantics.
      operationId: androidenterprise.storelayoutpages.patch
      x-api-path-slug: enterprisesenterpriseidstorelayoutpagespageid-patch
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: enterpriseId
        description: The ID of the enterprise
      - in: path
        name: pageId
        description: The ID of the page
      responses:
        200:
          description: OK
      tags:
      - Store Layout Page
    put:
      summary: Create Store Layout Page
      description: Updates the content of a store page.
      operationId: androidenterprise.storelayoutpages.update
      x-api-path-slug: enterprisesenterpriseidstorelayoutpagespageid-put
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: enterpriseId
        description: The ID of the enterprise
      - in: path
        name: pageId
        description: The ID of the page
      responses:
        200:
          description: OK
      tags:
      - Store Layout Page Cluster
  /{packageName}/purchases/subscriptions/{subscriptionId}/tokens/{token}:
    get:
      summary: Check User Subscriptions
      description: Checks whether a user's subscription purchase is valid and returns
        its expiry time.
      operationId: androidpublisher.purchases.subscriptions.get
      x-api-path-slug: packagenamepurchasessubscriptionssubscriptionidtokenstoken-get
      parameters:
      - in: path
        name: packageName
        description: The package name of the application for which this subscription
          was purchased (for example, com
      - in: path
        name: subscriptionId
        description: The purchased subscription ID (for example, monthly001)
      - in: path
        name: token
        description: The token provided to the users device when the subscription
          was purchased
      responses:
        200:
          description: OK
      tags:
      - Subscription
  /{packageName}/purchases/subscriptions/{subscriptionId}/tokens/{token}:cancel:
    post:
      summary: Cancel User Subscription
      description: Cancels a user's subscription purchase. The subscription remains
        valid until its expiration time.
      operationId: androidpublisher.purchases.subscriptions.cancel
      x-api-path-slug: packagenamepurchasessubscriptionssubscriptionidtokenstokencancel-post
      parameters:
      - in: path
        name: packageName
        description: The package name of the application for which this subscription
          was purchased (for example, com
      - in: path
        name: subscriptionId
        description: The purchased subscription ID (for example, monthly001)
      - in: path
        name: token
        description: The token provided to the users device when the subscription
          was purchased
      responses:
        200:
          description: OK
      tags:
      - Subscription
  /{packageName}/purchases/subscriptions/{subscriptionId}/tokens/{token}:defer:
    post:
      summary: Defer User Subscription
      description: Defers a user's subscription purchase until a specified future
        expiration time.
      operationId: androidpublisher.purchases.subscriptions.defer
      x-api-path-slug: packagenamepurchasessubscriptionssubscriptionidtokenstokendefer-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: packageName
        description: The package name of the application for which this subscription
          was purchased (for example, com
      - in: path
        name: subscriptionId
        description: The purchased subscription ID (for example, monthly001)
      - in: path
        name: token
        description: The token provided to the users device when the subscription
          was purchased
      responses:
        200:
          description: OK
      tags:
      - Subscription
  /enterprises/{enterpriseId}/storeLayout/pages/{pageId}/clusters:
    get:
      summary: Get Store Layout Page Clusters
      description: Retrieves the details of all clusters on the specified page.
      operationId: androidenterprise.storelayoutclusters.list
      x-api-path-slug: enterprisesenterpriseidstorelayoutpagespageidclusters-get
      parameters:
      - in: path
        name: enterpriseId
        description: The ID of the enterprise
      - in: path
        name: pageId
        description: The ID of the page
      responses:
        200:
          description: OK
      tags:
      - Store Layout Page Cluster
    post:
      summary: Insert Store Layout Page Cluster
      description: Inserts a new cluster in a page.
      operationId: androidenterprise.storelayoutclusters.insert
      x-api-path-slug: enterprisesenterpriseidstorelayoutpagespageidclusters-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: enterpriseId
        description: The ID of the enterprise
      - in: path
        name: pageId
        description: The ID of the page
      responses:
        200:
          description: OK
      tags:
      - Store Layout Page Cluster
  /{packageName}/purchases/subscriptions/{subscriptionId}/tokens/{token}:refund:
    post:
      summary: Refund User Subscription
      description: Refunds a user's subscription purchase, but the subscription remains
        valid until its expiration time and it will continue to recur.
      operationId: androidpublisher.purchases.subscriptions.refund
      x-api-path-slug: packagenamepurchasessubscriptionssubscriptionidtokenstokenrefund-post
      parameters:
      - in: path
        name: packageName
        description: The package name of the application for which this subscription
          was purchased (for example, com
      - in: path
        name: subscriptionId
        description: The purchased subscription ID (for example, monthly001)
      - in: path
        name: token
        description: The token provided to the users device when the subscription
          was purchased
      responses:
        200:
          description: OK
      tags:
      - Subscription
  /enterprises/{enterpriseId}/storeLayout/pages/{pageId}/clusters/{clusterId}:
    delete:
      summary: Delete Store Layout Page Cluster
      description: Deletes a cluster.
      operationId: androidenterprise.storelayoutclusters.delete
      x-api-path-slug: enterprisesenterpriseidstorelayoutpagespageidclustersclusterid-delete
      parameters:
      - in: path
        name: clusterId
        description: The ID of the cluster
      - in: path
        name: enterpriseId
        description: The ID of the enterprise
      - in: path
        name: pageId
        description: The ID of the page
      responses:
        200:
          description: OK
      tags:
      - Store Layout Page Cluster
    get:
      summary: Get Store Layout Page Cluster
      description: Retrieves details of a cluster.
      operationId: androidenterprise.storelayoutclusters.get
      x-api-path-slug: enterprisesenterpriseidstorelayoutpagespageidclustersclusterid-get
      parameters:
      - in: path
        name: clusterId
        description: The ID of the cluster
      - in: path
        name: enterpriseId
        description: The ID of the enterprise
      - in: path
        name: pageId
        description: The ID of the page
      responses:
        200:
          description: OK
      tags:
      - Store Layout Page Cluster
    patch:
      summary: Update Store Layout Page Cluster
      description: Updates a cluster. This method supports patch semantics.
      operationId: androidenterprise.storelayoutclusters.patch
      x-api-path-slug: enterprisesenterpriseidstorelayoutpagespageidclustersclusterid-patch
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: clusterId
        description: The ID of the cluster
      - in: path
        name: enterpriseId
        description: The ID of the enterprise
      - in: path
        name: pageId
        description: The ID of the page
      responses:
        200:
          description: OK
      tags:
      - Store Layout Page Cluster
    put:
      summary: Update Store Layout Page Cluster
      description: Updates a cluster.
      operationId: androidenterprise.storelayoutclusters.update
      x-api-path-slug: enterprisesenterpriseidstorelayoutpagespageidclustersclusterid-put
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: clusterId
        description: The ID of the cluster
      - in: path
        name: enterpriseId
        description: The ID of the enterprise
      - in: path
        name: pageId
        description: The ID of the page
      responses:
        200:
          description: OK
      tags:
      - Store Layout Page Cluster
  /{packageName}/purchases/subscriptions/{subscriptionId}/tokens/{token}:revoke:
    post:
      summary: Refunds and Revoke
      description: Refunds and immediately revokes a user's subscription purchase.
        Access to the subscription will be terminated immediately and it will stop
        recurring.
      operationId: androidpublisher.purchases.subscriptions.revoke
      x-api-path-slug: packagenamepurchasessubscriptionssubscriptionidtokenstokenrevoke-post
      parameters:
      - in: path
        name: packageName
        description: The package name of the application for which this subscription
          was purchased (for example, com
      - in: path
        name: subscriptionId
        description: The purchased subscription ID (for example, monthly001)
      - in: path
        name: token
        description: The token provided to the users device when the subscription
          was purchased
      responses:
        200:
          description: OK
      tags:
      - Subscription
  /{packageName}/purchases/voidedpurchases:
    get:
      summary: List Cancelled Purches
      description: Lists the purchases that were cancelled, refunded or charged-back.
      operationId: androidpublisher.purchases.voidedpurchases.list
      x-api-path-slug: packagenamepurchasesvoidedpurchases-get
      parameters:
      - in: query
        name: endTime
        description: The time, in milliseconds since the Epoch, of the newest voided
          in-app product purchase that you want to see in the response
      - in: query
        name: maxResults
      - in: path
        name: packageName
        description: The package name of the application for which voided purchases
          need to be returned (for example, com
      - in: query
        name: startIndex
      - in: query
        name: startTime
        description: The time, in milliseconds since the Epoch, of the oldest voided
          in-app product purchase that you want to see in the response
      - in: query
        name: token
      responses:
        200:
          description: OK
      tags:
      - Subscription
  /{packageName}/reviews:
    get:
      summary: Get Reviews
      description: Returns a list of reviews. Only reviews from last week will be
        returned.
      operationId: androidpublisher.reviews.list
      x-api-path-slug: packagenamereviews-get
      parameters:
      - in: query
        name: maxResults
      - in: path
        name: packageName
        description: Unique identifier for the Android app for which we want reviews;
          for example, com
      - in: query
        name: startIndex
      - in: query
        name: token
      - in: query
        name: translationLanguage
      responses:
        200:
          description: OK
      tags:
      - Reviews
  /enterprises/{enterpriseId}/unenroll:
    post:
      summary: Unenroll Enterprise
      description: Unenrolls an enterprise from the calling EMM.
      operationId: androidenterprise.enterprises.unenroll
      x-api-path-slug: enterprisesenterpriseidunenroll-post
      parameters:
      - in: path
        name: enterpriseId
        description: The ID of the enterprise
      responses:
        200:
          description: OK
      tags:
      - Enterprise
  /{packageName}/reviews/{reviewId}:
    get:
      summary: Get Review
      description: Returns a single review.
      operationId: androidpublisher.reviews.get
      x-api-path-slug: packagenamereviewsreviewid-get
      parameters:
      - in: path
        name: packageName
        description: Unique identifier for the Android app for which we want reviews;
          for example, com
      - in: path
        name: reviewId
      - in: query
        name: translationLanguage
      responses:
        200:
          description: OK
      tags:
      - Reviews
  /enterprises/{enterpriseId}/users:
    get:
      summary: Lookup User
      description: Looks up a user by primary email address. This is only supported
        for Google-managed users. Lookup of the id is not needed for EMM-managed users
        because the id is already returned in the result of the Users.insert call.
      operationId: androidenterprise.users.list
      x-api-path-slug: enterprisesenterpriseidusers-get
      parameters:
      - in: query
        name: email
        description: The exact primary email address of the user to look up
      - in: path
        name: enterpriseId
        description: The ID of the enterprise
      responses:
        200:
          description: OK
      tags:
      - User
    post:
      summary: Create New User
      description: |-
        Creates a new EMM-managed user.

        The Users resource passed in the body of the request should include an accountIdentifier and an accountType.
        If a corresponding user already exists with the same account identifier, the user will be updated with the resource. In this case only the displayName field can be changed.
      operationId: androidenterprise.users.insert
      x-api-path-slug: enterprisesenterpriseidusers-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: enterpriseId
        description: The ID of the enterprise
      responses:
        200:
          description: OK
      tags:
      - User
  /{packageName}/reviews/{reviewId}:reply:
    post:
      summary: Reply To Review
      description: Reply to a single review, or update an existing reply.
      operationId: androidpublisher.reviews.reply
      x-api-path-slug: packagenamereviewsreviewidreply-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: packageName
        description: Unique identifier for the Android app for which we want reviews;
          for example, com
      - in: path
        name: reviewId
      responses:
        200:
          description: OK
      tags:
      - Reviews
  /enterprises/{enterpriseId}/users/{userId}:
    delete:
      summary: Delete User
      description: Deleted an EMM-managed user.
      operationId: androidenterprise.users.delete
      x-api-path-slug: enterprisesenterpriseidusersuserid-delete
      parameters:
      - in: path
        name: enterpriseId
        description: The ID of the enterprise
      - in: path
        name: userId
        description: The ID of the user
      responses:
        200:
          description: OK
      tags:
      - User
    get:
      summary: Get User
      description: Retrieves a user's details.
      operationId: androidenterprise.users.get
      x-api-path-slug: enterprisesenterpriseidusersuserid-get
      parameters:
      - in: path
        name: enterpriseId
        description: The ID of the enterprise
      - in: path
        name: userId
        description: The ID of the user
      responses:
        200:
          description: OK
      tags:
      - User
    patch:
      summary: Update User
      description: |-
        Updates the details of an EMM-managed user.

        Can be used with EMM-managed users only (not Google managed users). Pass the new details in the Users resource in the request body. Only the displayName field can be changed. Other fields must either be unset or have the currently active value. This method supports patch semantics.
      operationId: androidenterprise.users.patch
      x-api-path-slug: enterprisesenterpriseidusersuserid-patch
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: enterpriseId
        description: The ID of the enterprise
      - in: path
        name: userId
        description: The ID of the user
      responses:
        200:
          description: OK
      tags:
      - User
    put:
      summary: Update User
      description: |-
        Updates the details of an EMM-managed user.

        Can be used with EMM-managed users only (not Google managed users). Pass the new details in the Users resource in the request body. Only the displayName field can be changed. Other fields must either be unset or have the currently active value.
      operationId: androidenterprise.users.update
      x-api-path-slug: enterprisesenterpriseidusersuserid-put
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: enterpriseId
        description: The ID of the enterprise
      - in: path
        name: userId
        description: The ID of the user
      responses:
        200:
          description: OK
      tags:
      - User
  /enterprises/{enterpriseId}/users/{userId}/authenticationToken:
    post:
      summary: Generate Authentication Token
      description: |-
        Generates an authentication token which the device policy client can use to provision the given EMM-managed user account on a device. The generated token is single-use and expires after a few minutes.

        This call only works with EMM-managed accounts.
      operationId: androidenterprise.users.generateAuthenticationToken
      x-api-path-slug: enterprisesenterpriseidusersuseridauthenticationtoken-post
      parameters:
      - in: path
        name: enterpriseId
        description: The ID of the enterprise
      - in: path
        name: userId
        description: The ID of the user
      responses:
        200:
          description: OK
      tags:
      - Token
  /enterprises/{enterpriseId}/users/{userId}/availableProductSet:
    get:
      summary: Get Products
      description: Retrieves the set of products a user is entitled to access.
      operationId: androidenterprise.users.getAvailableProductSet
      x-api-path-slug: enterprisesenterpriseidusersuseridavailableproductset-get
      parameters:
      - in: path
        name: enterpriseId
        description: The ID of the enterprise
      - in: path
        name: userId
        description: The ID of the user
      responses:
        200:
          description: OK
      tags:
      - Product
    put:
      summary: Update Products
      description: Modifies the set of products that a user is entitled to access
        (referred to as whitelisted products). Only products that are approved or
        products that were previously approved (products with revoked approval) can
        be whitelisted.
      operationId: androidenterprise.users.setAvailableProductSet
      x-api-path-slug: enterprisesenterpriseidusersuseridavailableproductset-put
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: enterpriseId
        description: The ID of the enterprise
      - in: path
        name: userId
        description: The ID of the user
      responses:
        200:
          description: OK
      tags:
      - Product
  /enterprises/{enterpriseId}/users/{userId}/devices:
    get:
      summary: Get User Devices
      description: Retrieves the IDs of all of a user's devices.
      operationId: androidenterprise.devices.list
      x-api-path-slug: enterprisesenterpriseidusersuseriddevices-get
      parameters:
      - in: path
        name: enterpriseId
        description: The ID of the enterprise
      - in: path
        name: userId
        description: The ID of the user
      responses:
        200:
          description: OK
      tags:
      - Device
  /enterprises/{enterpriseId}/users/{userId}/devices/{deviceId}:
    get:
      summary: Get User Device
      description: Retrieves the details of a device.
      operationId: androidenterprise.devices.get
      x-api-path-slug: enterprisesenterpriseidusersuseriddevicesdeviceid-get
      parameters:
      - in: path
        name: deviceId
        description: The ID of the device
      - in: path
        name: enterpriseId
        description: The ID of the enterprise
      - in: path
        name: userId
        description: The ID of the user
      responses:
        200:
          description: OK
      tags:
      - Device
  /enterprises/{enterpriseId}/users/{userId}/devices/{deviceId}/installs:
    get:
      summary: Get App Installs
      description: Retrieves the details of all apps installed on the specified device.
      operationId: androidenterprise.installs.list
      x-api-path-slug: enterprisesenterpriseidusersuseriddevicesdeviceidinstalls-get
      parameters:
      - in: path
        name: deviceId
        description: The Android ID of the device
      - in: path
        name: enterpriseId
        description: The ID of the enterprise
      - in: path
        name: userId
        description: The ID of the user
      responses:
        200:
          description: OK
      tags:
      - App Install
  /enterprises/{enterpriseId}/users/{userId}/devices/{deviceId}/installs/{installId}:
    delete:
      summary: Remove App Install
      description: Requests to remove an app from a device. A call to get or list
        will still show the app as installed on the device until it is actually removed.
      operationId: androidenterprise.installs.delete
      x-api-path-slug: enterprisesenterpriseidusersuseriddevicesdeviceidinstallsinstallid-delete
      parameters:
      - in: path
        name: deviceId
        description: The Android ID of the device
      - in: path
        name: enterpriseId
        description: The ID of the enterprise
      - in: path
        name: installId
        description: The ID of the product represented by the install, e
      - in: path
        name: userId
        description: The ID of the user
      responses:
        200:
          description: OK
      tags:
      - App Install
    get:
      summary: Get App Install
      description: Retrieves details of an installation of an app on a device.
      operationId: androidenterprise.installs.get
      x-api-path-slug: enterprisesenterpriseidusersuseriddevicesdeviceidinstallsinstallid-get
      parameters:
      - in: path
        name: deviceId
        description: The Android ID of the device
      - in: path
        name: enterpriseId
        description: The ID of the enterprise
      - in: path
        name: installId
        description: The ID of the product represented by the install, e
      - in: path
        name: userId
        description: The ID of the user
      responses:
        200:
          description: OK
      tags:
      - App Install
    patch:
      summary: Update App Install
      description: Requests to install the latest version of an app to a device. If
        the app is already installed, then it is updated to the latest version if
        necessary. This method supports patch semantics.
      operationId: androidenterprise.installs.patch
      x-api-path-slug: enterprisesenterpriseidusersuseriddevicesdeviceidinstallsinstallid-patch
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: deviceId
        description: The Android ID of the device
      - in: path
        name: enterpriseId
        description: The ID of the enterprise
      - in: path
        name: installId
        description: The ID of the product represented by the install, e
      - in: path
        name: userId
        description: The ID of the user
      responses:
        200:
          description: OK
      tags:
      - App Install
    put:
      summary: Update App Install
      description: Requests to install the latest version of an app to a device. If
        the app is already installed, then it is updated to the latest version if
        necessary.
      operationId: androidenterprise.installs.update
      x-api-path-slug: enterprisesenterpriseidusersuseriddevicesdeviceidinstallsinstallid-put
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: deviceId
        description: The Android ID of the device
      - in: path
        name: enterpriseId
        description: The ID of the enterprise
      - in: path
        name: installId
        description: The ID of the product represented by the install, e
      - in: path
        name: userId
        description: The ID of the user
      responses:
        200:
          description: OK
      tags:
      - App Install
  /enterprises/{enterpriseId}/users/{userId}/devices/{deviceId}/managedConfigurationsForDevice:
    get:
      summary: Get Per Device App Installs
      description: Lists all the per-device managed configurations for the specified
        device. Only the ID is set.
      operationId: androidenterprise.managedconfigurationsfordevice.list
      x-api-path-slug: enterprisesenterpriseidusersuseriddevicesdeviceidmanagedconfigurationsfordevice-get
      parameters:
      - in: path
        name: deviceId
        description: The Android ID of the device
      - in: path
        name: enterpriseId
        description: The ID of the enterprise
      - in: path
        name: userId
        description: The ID of the user
      responses:
        200:
          description: OK
      tags:
      - App Install
  /enterprises/{enterpriseId}/users/{userId}/devices/{deviceId}/managedConfigurationsForDevice/{managedConfigurationForDeviceId}:
    delete:
      summary: Remove Per Device App Install
      description: Removes a per-device managed configuration for an app for the specified
        device.
      operationId: androidenterprise.managedconfigurationsfordevice.delete
      x-api-path-slug: enterprisesenterpriseidusersuseriddevicesdeviceidmanagedconfigurationsfordevicemanagedconfigurationfordeviceid-delete
      parameters:
      - in: path
        name: deviceId
        description: The Android ID of the device
      - in: path
        name: enterpriseId
        description: The ID of the enterprise
      - in: path
        name: managedConfigurationForDeviceId
        description: The ID of the managed configuration (a product ID), e
      - in: path
        name: userId
        description: The ID of the user
      responses:
        200:
          description: OK
      tags:
      - App Install
    get:
      summary: Get Per Device App Install
      description: Retrieves details of a per-device managed configuration.
      operationId: androidenterprise.managedconfigurationsfordevice.get
      x-api-path-slug: enterprisesenterpriseidusersuseriddevicesdeviceidmanagedconfigurationsfordevicemanagedconfigurationfordeviceid-get
      parameters:
      - in: path
        name: deviceId
        description: The Android ID of the device
      - in: path
        name: enterpriseId
        description: The ID of the enterprise
      - in: path
        name: managedConfigurationForDeviceId
        description: The ID of the managed configuration (a product ID), e
      - in: path
        name: userId
        description: The ID of the user
      responses:
        200:
          description: OK
      tags:
      - App Install
    patch:
      summary: Update Per Device App Install
      description: Adds or updates a per-device managed configuration for an app for
        the specified device. This method supports patch semantics.
      operationId: androidenterprise.managedconfigurationsfordevice.patch
      x-api-path-slug: enterprisesenterpriseidusersuseriddevicesdeviceidmanagedconfigurationsfordevicemanagedconfigurationfordeviceid-patch
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: deviceId
        description: The Android ID of the device
      - in: path
        name: enterpriseId
        description: The ID of the enterprise
      - in: path
        name: managedConfigurationForDeviceId
        description: The ID of the managed configuration (a product ID), e
      - in: path
        name: userId
        description: The ID of the user
      responses:
        200:
          description: OK
      tags:
      - App Install
    put:
      summary: Update Per Device App Install
      description: Adds or updates a per-device managed configuration for an app for
        the specified device.
      operationId: androidenterprise.managedconfigurationsfordevice.update
      x-api-path-slug: enterprisesenterpriseidusersuseriddevicesdeviceidmanagedconfigurationsfordevicemanagedconfigurationfordeviceid-put
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: deviceId
        description: The Android ID of the device
      - in: path
        name: enterpriseId
        description: The ID of the enterprise
      - in: path
        name: managedConfigurationForDeviceId
        description: The ID of the managed configuration (a product ID), e
      - in: path
        name: userId
        description: The ID of the user
      responses:
        200:
          description: OK
      tags:
      - App Install
  /enterprises/{enterpriseId}/users/{userId}/devices/{deviceId}/state:
    get:
      summary: Get Per Device App Install State
      description: Retrieves whether a device's access to Google services is enabled
        or disabled. The device state takes effect only if enforcing EMM policies
        on Android devices is enabled in the Google Admin Console. Otherwise, the
        device state is ignored and all devices are allowed access to Google services.
        This is only supported for Google-managed users.
      operationId: androidenterprise.devices.getState
      x-api-path-slug: enterprisesenterpriseidusersuseriddevicesdeviceidstate-get
      parameters:
      - in: path
        name: deviceId
        description: The ID of the device
      - in: path
        name: enterpriseId
        description: The ID of the enterprise
      - in: path
        name: userId
        description: The ID of the user
      responses:
        200:
          description: OK
      tags:
      - App Install
    put:
      summary: Update Per Device App Install State
      description: Sets whether a device's access to Google services is enabled or
        disabled. The device state takes effect only if enforcing EMM policies on
        Android devices is enabled in the Google Admin Console. Otherwise, the device
        state is ignored and all devices are allowed access to Google services. This
        is only supported for Google-managed users.
      operationId: androidenterprise.devices.setState
      x-api-path-slug: enterprisesenterpriseidusersuseriddevicesdeviceidstate-put
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: deviceId
        description: The ID of the device
      - in: path
        name: enterpriseId
        description: The ID of the enterprise
      - in: path
        name: userId
        description: The ID of the user
      responses:
        200:
          description: OK
      tags:
      - App Install
  /enterprises/{enterpriseId}/users/{userId}/entitlements:
    get:
      summary: Get Entitlements
      description: Lists all entitlements for the specified user. Only the ID is set.
      operationId: androidenterprise.entitlements.list
      x-api-path-slug: enterprisesenterpriseidusersuseridentitlements-get
      parameters:
      - in: path
        name: enterpriseId
        description: The ID of the enterprise
      - in: path
        name: userId
        description: The ID of the user
      responses:
        200:
          description: OK
      tags:
      - Entitlement
  /enterprises/{enterpriseId}/users/{userId}/entitlements/{entitlementId}:
    delete:
      summary: Remove Entitlement
      description: Removes an entitlement to an app for a user.
      operationId: androidenterprise.entitlements.delete
      x-api-path-slug: enterprisesenterpriseidusersuseridentitlementsentitlementid-delete
      parameters:
      - in: path
        name: enterpriseId
        description: The ID of the enterprise
      - in: path
        name: entitlementId
        description: The ID of the entitlement (a product ID), e
      - in: path
        name: userId
        description: The ID of the user
      responses:
        200:
          description: OK
      tags:
      - Entitlement
    get:
      summary: Get Entitlement
      description: Retrieves details of an entitlement.
      operationId: androidenterprise.entitlements.get
      x-api-path-slug: enterprisesenterpriseidusersuseridentitlementsentitlementid-get
      parameters:
      - in: path
        name: enterpriseId
        description: The ID of the enterprise
      - in: path
        name: entitlementId
        description: The ID of the entitlement (a product ID), e
      - in: path
        name: userId
        description: The ID of the user
      responses:
        200:
          description: OK
      tags:
      - Entitlement
    patch:
      summary: Update Entitlement
      description: Adds or updates an entitlement to an app for a user. This method
        supports patch semantics.
      operationId: androidenterprise.entitlements.patch
      x-api-path-slug: enterprisesenterpriseidusersuseridentitlementsentitlementid-patch
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
        description: Set to true to also install the product on all the users devices
          where possible
      - in: path
        name: userId
        description: The ID of the user
      responses:
        200:
          description: OK
      tags:
      - Entitlement
    put:
      summary: Update Entitlement
      description: Adds or updates an entitlement to an app for a user.
      operationId: androidenterprise.entitlements.update
      x-api-path-slug: enterprisesenterpriseidusersuseridentitlementsentitlementid-put
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
        description: Set to true to also install the product on all the users devices
          where possible
      - in: path
        name: userId
        description: The ID of the user
      responses:
        200:
          description: OK
      tags:
      - Entitlement
  /enterprises/{enterpriseId}/users/{userId}/managedConfigurationsForUser:
    get:
      summary: Get Per User Configurations
      description: Lists all the per-user managed configurations for the specified
        user. Only the ID is set.
      operationId: androidenterprise.managedconfigurationsforuser.list
      x-api-path-slug: enterprisesenterpriseidusersuseridmanagedconfigurationsforuser-get
      parameters:
      - in: path
        name: enterpriseId
        description: The ID of the enterprise
      - in: path
        name: userId
        description: The ID of the user
      responses:
        200:
          description: OK
      tags:
      - Configuration
  /enterprises/{enterpriseId}/users/{userId}/managedConfigurationsForUser/{managedConfigurationForUserId}:
    delete:
      summary: Delete Per User Configurations
      description: Removes a per-user managed configuration for an app for the specified
        user.
      operationId: androidenterprise.managedconfigurationsforuser.delete
      x-api-path-slug: enterprisesenterpriseidusersuseridmanagedconfigurationsforusermanagedconfigurationforuserid-delete
      parameters:
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
      - Configuration
    get:
      summary: Get Per User Configuration
      description: Retrieves details of a per-user managed configuration for an app
        for the specified user.
      operationId: androidenterprise.managedconfigurationsforuser.get
      x-api-path-slug: enterprisesenterpriseidusersuseridmanagedconfigurationsforusermanagedconfigurationforuserid-get
      parameters:
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
      - Configuration
    patch:
      summary: Update Per User Configuration
      description: Adds or updates a per-user managed configuration for an app for
        the specified user. This method supports patch semantics.
      operationId: androidenterprise.managedconfigurationsforuser.patch
      x-api-path-slug: enterprisesenterpriseidusersuseridmanagedconfigurationsforusermanagedconfigurationforuserid-patch
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
      - Configuration
    put:
      summary: Update Per User Configuration
      description: Adds or updates a per-user managed configuration for an app for
        the specified user.
      operationId: androidenterprise.managedconfigurationsforuser.update
      x-api-path-slug: enterprisesenterpriseidusersuseridmanagedconfigurationsforusermanagedconfigurationforuserid-put
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
      - Configuration
  /enterprises/{enterpriseId}/users/{userId}/token:
    delete:
      summary: Delete User Token
      description: Revokes a previously generated token (activation code) for the
        user.
      operationId: androidenterprise.users.revokeToken
      x-api-path-slug: enterprisesenterpriseidusersuseridtoken-delete
      parameters:
      - in: path
        name: enterpriseId
        description: The ID of the enterprise
      - in: path
        name: userId
        description: The ID of the user
      responses:
        200:
          description: OK
      tags:
      - Token
    post:
      summary: Generate User Token
      description: |-
        Generates a token (activation code) to allow this user to configure their managed account in the Android Setup Wizard. Revokes any previously generated token.

        This call only works with Google managed accounts.
      operationId: androidenterprise.users.generateToken
      x-api-path-slug: enterprisesenterpriseidusersuseridtoken-post
      parameters:
      - in: path
        name: enterpriseId
        description: The ID of the enterprise
      - in: path
        name: userId
        description: The ID of the user
      responses:
        200:
          description: OK
      tags:
      - Token
  /permissions/{permissionId}:
    get:
      summary: Get Permissions
      description: Retrieves details of an Android app permission for display to an
        enterprise admin.
      operationId: androidenterprise.permissions.get
      x-api-path-slug: permissionspermissionid-get
      parameters:
      - in: query
        name: language
        description: The BCP47 tag for the users preferred language (e
      - in: path
        name: permissionId
        description: The ID of the permission
      responses:
        200:
          description: OK
      tags:
      - Permission
  /states:
    get:
      summary: Get State Keys
      description: Lists all the states keys, and optionally the state data.
      operationId: appstate.states.list
      x-api-path-slug: states-get
      parameters:
      - in: query
        name: includeData
        description: Whether to include the full data in addition to the version number
      responses:
        200:
          description: OK
      tags:
      - Application State
  /states/{stateKey}:
    delete:
      summary: Delete State Key
      description: Deletes a key and the data associated with it. The key is removed
        and no longer counts against the key quota. Note that since this method is
        not safe in the face of concurrent modifications, it should only be used for
        development and testing purposes. Invoking this method in shipping code can
        result in data loss and data corruption.
      operationId: appstate.states.delete
      x-api-path-slug: statesstatekey-delete
      parameters:
      - in: path
        name: stateKey
        description: The key for the data to be retrieved
      responses:
        200:
          description: OK
      tags:
      - Application State
    get:
      summary: Get State Key
      description: Retrieves the data corresponding to the passed key. If the key
        does not exist on the server, an HTTP 404 will be returned.
      operationId: appstate.states.get
      x-api-path-slug: statesstatekey-get
      parameters:
      - in: path
        name: stateKey
        description: The key for the data to be retrieved
      responses:
        200:
          description: OK
      tags:
      - Application State
    put:
      summary: Update State Key
      description: Update the data associated with the input key if and only if the
        passed version matches the currently stored version. This method is safe in
        the face of concurrent writes. Maximum per-key size is 128KB.
      operationId: appstate.states.update
      x-api-path-slug: statesstatekey-put
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: currentStateVersion
        description: The version of the app state your application is attempting to
          update
      - in: path
        name: stateKey
        description: The key for the data to be retrieved
      responses:
        200:
          description: OK
      tags:
      - Application State
  /states/{stateKey}/clear:
    post:
      summary: Clear State Key
      description: Clears (sets to empty) the data for the passed key if and only
        if the passed version matches the currently stored version. This method results
        in a conflict error on version mismatch.
      operationId: appstate.states.clear
      x-api-path-slug: statesstatekeyclear-post
      parameters:
      - in: query
        name: currentDataVersion
        description: The version of the data to be cleared
      - in: path
        name: stateKey
        description: The key for the data to be retrieved
      responses:
        200:
          description: OK
      tags:
      - Application State
  /achievements:
    get:
      summary: Get Achievements
      description: Lists all the achievement definitions for your application.
      operationId: games.achievementDefinitions.list
      x-api-path-slug: achievements-get
      parameters:
      - in: query
        name: consistencyToken
        description: The last-seen mutation timestamp
      - in: query
        name: language
        description: The preferred language to use for strings returned by this method
      - in: query
        name: maxResults
        description: The maximum number of achievement resources to return in the
          response, used for paging
      - in: query
        name: pageToken
        description: The token returned by the previous request
      responses:
        200:
          description: OK
      tags:
      - Achievement
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