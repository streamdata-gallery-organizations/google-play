---
swagger: "2.0"
x-collection-name: Google Play
x-complete: 0
info:
  title: Google Play Get In App Product
  version: 1.0.0
  description: Returns information about the in-app product specified.
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