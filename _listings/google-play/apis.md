---
name: Google Play
x-slug: google-play
description: 'The Google Play Developer API allows you to perform a number of publishing
  and app-management tasks. It includes two components: The Subscriptions and In-App
  Purchases API lets you manage in-app purchases and subscriptions. The Publishing
  API lets you upload and publish apps, and perform other publishing-related tasks.'
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
x-kinRank: "9"
x-alexaRank: "0"
tags: Google Play
created: "2018-06-20"
modified: "2018-06-20"
url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/apis.md
specificationVersion: "0.14"
apis:
- name: Google Play Create App Edit
  x-api-slug: google-play
  description: Creates a new edit for an app, populated with the app's current state.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///{packageName}/edits
  tags: Application
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/packagenameedits-post-openapi.md
- name: Google Play Delete App Edit
  x-api-slug: google-play
  description: Deletes an edit for an app. Creating a new edit will automatically
    delete any of your previous edits so this method need only be called if you want
    to preemptively abandon an edit.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///{packageName}/edits/{editId}
  tags: Application
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/packagenameeditseditid-delete-openapi.md
- name: Google Play DGetelete App Edit
  x-api-slug: google-play
  description: Returns information about the edit specified. Calls will fail if the
    edit is no long active (e.g. has been deleted, superseded or expired).
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///{packageName}/edits/{editId}
  tags: Application
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/packagenameeditseditid-get-openapi.md
- name: Google Play Create APK
  x-api-slug: google-play
  description: Creates a new APK without uploading the APK itself to Google Play,
    instead hosting the APK at a specified URL. This function is only available to
    enterprises using Google Play for Work whose application is configured to restrict
    distribution to the enterprise domain.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///{packageName}/edits/{editId}/apks/externallyHosted
  tags: Application
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/packagenameeditseditidapksexternallyhosted-post-openapi.md
- name: Google Play Update Deobfuscation FIle
  x-api-slug: google-play
  description: Uploads the deobfuscation file of the specified APK. If a deobfuscation
    file already exists, it will be replaced.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///{packageName}/edits/{editId}/apks/{apkVersionCode}/deobfuscationFiles/{deobfuscationFileType}
  tags: Deobfuscation FIle
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/packagenameeditseditidapksapkversioncodedeobfuscationfilesdeobfuscationfiletype-post-openapi.md
- name: Google Play Get Expansion File
  x-api-slug: google-play
  description: Fetches the Expansion File configuration for the APK specified.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///{packageName}/edits/{editId}/apks/{apkVersionCode}/expansionFiles/{expansionFileType}
  tags: Expansion File
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/packagenameeditseditidapksapkversioncodeexpansionfilesexpansionfiletype-get-openapi.md
- name: Google Play Update APK Expansion File
  x-api-slug: google-play
  description: Updates the APK's Expansion File configuration to reference another
    APK's Expansion Files. To add a new Expansion File use the Upload method. This
    method supports patch semantics.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///{packageName}/edits/{editId}/apks/{apkVersionCode}/expansionFiles/{expansionFileType}
  tags: APK Expansion File
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/packagenameeditseditidapksapkversioncodeexpansionfilesexpansionfiletype-patch-openapi.md
- name: Google Play Upload APK Expansion File
  x-api-slug: google-play
  description: Uploads and attaches a new Expansion File to the APK specified.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///{packageName}/edits/{editId}/apks/{apkVersionCode}/expansionFiles/{expansionFileType}
  tags: APK Expansion File
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/packagenameeditseditidapksapkversioncodeexpansionfilesexpansionfiletype-post-openapi.md
- name: Google Play Update APK Expansion File
  x-api-slug: google-play
  description: Updates the APK's Expansion File configuration to reference another
    APK's Expansion Files. To add a new Expansion File use the Upload method.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///{packageName}/edits/{editId}/apks/{apkVersionCode}/expansionFiles/{expansionFileType}
  tags: APK Expansion File
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/packagenameeditseditidapksapkversioncodeexpansionfilesexpansionfiletype-put-openapi.md
- name: Google Play Delete All APK Localized Listing
  x-api-slug: google-play
  description: Deletes all the APK-specific localized listings for a specified APK.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///{packageName}/edits/{editId}/apks/{apkVersionCode}/listings
  tags: APK Localized Listing
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/packagenameeditseditidapksapkversioncodelistings-delete-openapi.md
- name: Google Play Get APK Localized Listings
  x-api-slug: google-play
  description: Lists all the APK-specific localized listings for a specified APK.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///{packageName}/edits/{editId}/apks/{apkVersionCode}/listings
  tags: APK Localized Listing
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/packagenameeditseditidapksapkversioncodelistings-get-openapi.md
- name: Google Play Delete APK Localized Listing
  x-api-slug: google-play
  description: Deletes the APK-specific localized listing for a specified APK and
    language code.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///{packageName}/edits/{editId}/apks/{apkVersionCode}/listings/{language}
  tags: APK Localized Listing
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/packagenameeditseditidapksapkversioncodelistingslanguage-delete-openapi.md
- name: Google Play Get APK Localized Listing
  x-api-slug: google-play
  description: Fetches the APK-specific localized listing for a specified APK and
    language code.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///{packageName}/edits/{editId}/apks/{apkVersionCode}/listings/{language}
  tags: APK Localized Listing
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/packagenameeditseditidapksapkversioncodelistingslanguage-get-openapi.md
- name: Google Play Update APK Localized Listing
  x-api-slug: google-play
  description: Updates or creates the APK-specific localized listing for a specified
    APK and language code. This method supports patch semantics.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///{packageName}/edits/{editId}/apks/{apkVersionCode}/listings/{language}
  tags: APK Localized Listing
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/packagenameeditseditidapksapkversioncodelistingslanguage-patch-openapi.md
- name: Google Play Update APK Localized Listing
  x-api-slug: google-play
  description: Updates or creates the APK-specific localized listing for a specified
    APK and language code.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///{packageName}/edits/{editId}/apks/{apkVersionCode}/listings/{language}
  tags: APK Localized Listing
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/packagenameeditseditidapksapkversioncodelistingslanguage-put-openapi.md
- name: Google Play Get App Detail
  x-api-slug: google-play
  description: Fetches app details for this edit. This includes the default language
    and developer support contact information.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///{packageName}/edits/{editId}/details
  tags: Application
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/packagenameeditseditiddetails-get-openapi.md
- name: Google Play Update App Detail
  x-api-slug: google-play
  description: Updates app details for this edit. This method supports patch semantics.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///{packageName}/edits/{editId}/details
  tags: Application
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/packagenameeditseditiddetails-patch-openapi.md
- name: Google Play Update App Detail
  x-api-slug: google-play
  description: Updates app details for this edit.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///{packageName}/edits/{editId}/details
  tags: Application
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/packagenameeditseditiddetails-put-openapi.md
- name: Google Play Delete App Detail
  x-api-slug: google-play
  description: Deletes all localized listings from an edit.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///{packageName}/edits/{editId}/listings
  tags: Application
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/packagenameeditseditidlistings-delete-openapi.md
- name: Google Play Get App Details
  x-api-slug: google-play
  description: Returns all of the localized store listings attached to this edit.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///{packageName}/edits/{editId}/listings
  tags: Application
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/packagenameeditseditidlistings-get-openapi.md
- name: Google Play Delete Localized Store Listing
  x-api-slug: google-play
  description: Deletes the specified localized store listing from an edit.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///{packageName}/edits/{editId}/listings/{language}
  tags: Localized Store Listing
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/packagenameeditseditidlistingslanguage-delete-openapi.md
- name: Google Play Get Localized Store Listing
  x-api-slug: google-play
  description: Fetches information about a localized store listing.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///{packageName}/edits/{editId}/listings/{language}
  tags: Localized Store Listing
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/packagenameeditseditidlistingslanguage-get-openapi.md
- name: Google Play Update Localized Store Listing
  x-api-slug: google-play
  description: Creates or updates a localized store listing. This method supports
    patch semantics.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///{packageName}/edits/{editId}/listings/{language}
  tags: Localized Store Listing
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/packagenameeditseditidlistingslanguage-patch-openapi.md
- name: Google Play Update Localized Store Listing
  x-api-slug: google-play
  description: Creates or updates a localized store listing.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///{packageName}/edits/{editId}/listings/{language}
  tags: Localized Store Listing
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/packagenameeditseditidlistingslanguage-put-openapi.md
- name: Google Play Delete All Images
  x-api-slug: google-play
  description: Deletes all images for the specified language and image type.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///{packageName}/edits/{editId}/listings/{language}/{imageType}
  tags: Image
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/packagenameeditseditidlistingslanguageimagetype-delete-openapi.md
- name: Google Play Get Enterprises
  x-api-slug: google-play
  description: Looks up an enterprise by domain name. This is only supported for enterprises
    created via the Google-initiated creation flow. Lookup of the id is not needed
    for enterprises created via the EMM-initiated flow since the EMM learns the enterprise
    ID in the callback specified in the Enterprises.generateSignupUrl call.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///enterprises
  tags: Enterprise
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/enterprises-get-openapi.md
- name: Google Play Get All Images
  x-api-slug: google-play
  description: Lists all images for the specified language and image type.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///{packageName}/edits/{editId}/listings/{language}/{imageType}
  tags: Image
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/packagenameeditseditidlistingslanguageimagetype-get-openapi.md
- name: Google Play Create Enterprise
  x-api-slug: google-play
  description: Establishes the binding between the EMM and an enterprise. This is
    now deprecated; use enroll instead.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///enterprises
  tags: Enterprise
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/enterprises-post-openapi.md
- name: Google Play Create Acknowledges Notification Set
  x-api-slug: google-play
  description: Acknowledges notifications that were received from Enterprises.PullNotificationSet
    to prevent subsequent calls from returning the same notifications.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///enterprises/acknowledgeNotificationSet
  tags: Notification
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/enterprisesacknowledgenotificationset-post-openapi.md
- name: Google Play Upoads Image
  x-api-slug: google-play
  description: Uploads a new image and adds it to the list of images for the specified
    language and image type.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///{packageName}/edits/{editId}/listings/{language}/{imageType}
  tags: Image
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/packagenameeditseditidlistingslanguageimagetype-post-openapi.md
- name: Google Play Complete Signup Flow
  x-api-slug: google-play
  description: Completes the signup flow, by specifying the Completion token and Enterprise
    token. This request must not be called multiple times for a given Enterprise Token.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///enterprises/completeSignup
  tags: Signup
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/enterprisescompletesignup-post-openapi.md
- name: Google Play Delete Image
  x-api-slug: google-play
  description: Deletes the image (specified by id) from the edit.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///{packageName}/edits/{editId}/listings/{language}/{imageType}/{imageId}
  tags: Image
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/packagenameeditseditidlistingslanguageimagetypeimageid-delete-openapi.md
- name: Google Play Entroll Enterprise
  x-api-slug: google-play
  description: Enrolls an enterprise with the calling EMM.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///enterprises/enroll
  tags: Enroll
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/enterprisesenroll-post-openapi.md
- name: Google Play Get Notification Set
  x-api-slug: google-play
  description: |-
    Pulls and returns a notification set for the enterprises associated with the service account authenticated for the request. The notification set may be empty if no notification are pending.
    A notification set returned needs to be acknowledged within 20 seconds by calling Enterprises.AcknowledgeNotificationSet, unless the notification set is empty.
    Notifications that are not acknowledged within the 20 seconds will eventually be included again in the response to another PullNotificationSet request, and those that are never acknowledged will ultimately be deleted according to the Google Cloud Platform Pub/Sub system policy.
    Multiple requests might be performed concurrently to retrieve notifications, in which case the pending notifications (if any) will be split among each caller, if any are pending.
    If no notifications are present, an empty notification list is returned. Subsequent requests may return more notifications once they become available.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///enterprises/pullNotificationSet
  tags: Notification
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/enterprisespullnotificationset-post-openapi.md
- name: 'Google Play '
  x-api-slug: google-play
  description: Generates a sign-up URL.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///enterprises/signupUrl
  tags: Signup
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/enterprisessignupurl-post-openapi.md
- name: Google Play Delete Enterprise
  x-api-slug: google-play
  description: Deletes the binding between the EMM and enterprise. This is now deprecated.
    Use this method only to unenroll customers that were previously enrolled with
    the insert call, then enroll them again with the enroll call.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///enterprises/{enterpriseId}
  tags: Enterprise
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/enterprisesenterpriseid-delete-openapi.md
- name: Google Play Get Enterprise
  x-api-slug: google-play
  description: Retrieves the name and domain of an enterprise.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///enterprises/{enterpriseId}
  tags: Enterprise
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/enterprisesenterpriseid-get-openapi.md
- name: Google Play Update Enterprise Account
  x-api-slug: google-play
  description: Sets the account that will be used to authenticate to the API as the
    enterprise.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///enterprises/{enterpriseId}/account
  tags: Enterprise
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/enterprisesenterpriseidaccount-put-openapi.md
- name: Google Play Create Web Token
  x-api-slug: google-play
  description: Returns a unique token to access an embeddable UI. To generate a web
    UI, pass the generated token into the managed Google Play javascript API. Each
    token may only be used to start one UI session. See the javascript API documentation
    for further information.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///enterprises/{enterpriseId}/createWebToken
  tags: Token
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/enterprisesenterpriseidcreatewebtoken-post-openapi.md
- name: Google Play Get Group Licenses
  x-api-slug: google-play
  description: Retrieves IDs of all products for which the enterprise has a group
    license.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///enterprises/{enterpriseId}/groupLicenses
  tags: License
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/enterprisesenterpriseidgrouplicenses-get-openapi.md
- name: Google Play Get Group License
  x-api-slug: google-play
  description: Retrieves details of an enterprise's group license for a product.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///enterprises/{enterpriseId}/groupLicenses/{groupLicenseId}
  tags: License
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/enterprisesenterpriseidgrouplicensesgrouplicenseid-get-openapi.md
- name: Google Play Get Track Configurations
  x-api-slug: google-play
  description: Lists all the track configurations for this edit.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///{packageName}/edits/{editId}/tracks
  tags: Track Configuration
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/packagenameeditseditidtracks-get-openapi.md
- name: Google Play Get Group License User
  x-api-slug: google-play
  description: Retrieves the IDs of the users who have been granted entitlements under
    the license.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///enterprises/{enterpriseId}/groupLicenses/{groupLicenseId}/users
  tags: License
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/enterprisesenterpriseidgrouplicensesgrouplicenseidusers-get-openapi.md
- name: Google Play Get Track Configuration
  x-api-slug: google-play
  description: Fetches the track configuration for the specified track type. Includes
    the APK version codes that are in this track.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///{packageName}/edits/{editId}/tracks/{track}
  tags: Track Configuration
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/packagenameeditseditidtrackstrack-get-openapi.md
- name: Google Play Get Products
  x-api-slug: google-play
  description: Finds approved products that match a query, or all approved products
    if there is no query.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///enterprises/{enterpriseId}/products
  tags: Product
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/enterprisesenterpriseidproducts-get-openapi.md
- name: Google Play Update Track Configuration
  x-api-slug: google-play
  description: Updates the track configuration for the specified track type. When
    halted, the rollout track cannot be updated without adding new APKs, and adding
    new APKs will cause it to resume. This method supports patch semantics.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///{packageName}/edits/{editId}/tracks/{track}
  tags: Track Configuration
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/packagenameeditseditidtrackstrack-patch-openapi.md
- name: Google Play Update Track Configuration
  x-api-slug: google-play
  description: Updates the track configuration for the specified track type. When
    halted, the rollout track cannot be updated without adding new APKs, and adding
    new APKs will cause it to resume.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///{packageName}/edits/{editId}/tracks/{track}
  tags: Track Configuration
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/packagenameeditseditidtrackstrack-put-openapi.md
- name: Google Play Get Product
  x-api-slug: google-play
  description: Retrieves details of a product for display to an enterprise admin.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///enterprises/{enterpriseId}/products/{productId}
  tags: Product
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/enterprisesenterpriseidproductsproductid-get-openapi.md
- name: Google Play Get Restriction Schema
  x-api-slug: google-play
  description: Retrieves the schema that defines the configurable properties for this
    product. All products have a schema, but this schema may be empty if no managed
    configurations have been defined. This schema can be used to populate a UI that
    allows an admin to configure the product. To apply a managed configuration based
    on the schema obtained using this API, see Managed Configurations through Play.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///enterprises/{enterpriseId}/products/{productId}/appRestrictionsSchema
  tags: Schema
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/enterprisesenterpriseidproductsproductidapprestrictionsschema-get-openapi.md
- name: Google Play Commit Changes
  x-api-slug: google-play
  description: Commits/applies the changes made in this edit back to the app.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///{packageName}/edits/{editId}:commit
  tags: Change
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/packagenameeditseditidcommit-post-openapi.md
- name: Google Play Validate Changes
  x-api-slug: google-play
  description: Checks that the edit can be successfully committed. The edit's changes
    are not applied to the live app.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///{packageName}/edits/{editId}:validate
  tags: Change
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/packagenameeditseditidvalidate-post-openapi.md
- name: Google Play Approve Product
  x-api-slug: google-play
  description: |-
    Approves the specified product and the relevant app permissions, if any. The maximum number of products that you can approve per enterprise customer is 1,000.

    To learn how to use managed Google Play to design and create a store layout to display approved products to your users, see Store Layout Design.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///enterprises/{enterpriseId}/products/{productId}/approve
  tags: Product
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/enterprisesenterpriseidproductsproductidapprove-post-openapi.md
- name: Google Play Get Entitlements
  x-api-slug: google-play
  description: Lists the user's current inapp item or subscription entitlements
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///{packageName}/entitlements
  tags: Entitlement
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/packagenameentitlements-get-openapi.md
- name: Google Play Generates a URL
  x-api-slug: google-play
  description: |-
    Generates a URL that can be rendered in an iframe to display the permissions (if any) of a product. An enterprise admin must view these permissions and accept them on behalf of their organization in order to approve that product.

    Admins should accept the displayed permissions by interacting with a separate UI element in the EMM console, which in turn should trigger the use of this URL as the approvalUrlInfo.approvalUrl property in a Products.approve call to approve the product. This URL can only be used to display permissions for up to 1 day.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///enterprises/{enterpriseId}/products/{productId}/generateApprovalUrl
  tags: URL
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/enterprisesenterpriseidproductsproductidgenerateapprovalurl-post-openapi.md
- name: Google Play Retrieves the Android App Permission
  x-api-slug: google-play
  description: Retrieves the Android app permissions required by this app.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///enterprises/{enterpriseId}/products/{productId}/permissions
  tags: Permission
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/enterprisesenterpriseidproductsproductidpermissions-get-openapi.md
- name: Google Play Get In App Products
  x-api-slug: google-play
  description: List all the in-app products for an Android app, both subscriptions
    and managed in-app products..
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///{packageName}/inappproducts
  tags: In App Product
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/packagenameinappproducts-get-openapi.md
- name: Google Play Unnarove Product
  x-api-slug: google-play
  description: Unapproves the specified product (and the relevant app permissions,
    if any)
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///enterprises/{enterpriseId}/products/{productId}/unapprove
  tags: Product
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/enterprisesenterpriseidproductsproductidunapprove-post-openapi.md
- name: Google Play Create In App Products
  x-api-slug: google-play
  description: Creates a new in-app product for an app.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///{packageName}/inappproducts
  tags: In App Product
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/packagenameinappproducts-post-openapi.md
- name: Google Play Send Test Push
  x-api-slug: google-play
  description: Sends a test push notification to validate the EMM integration with
    the Google Cloud Pub/Sub service for this enterprise.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///enterprises/{enterpriseId}/sendTestPushNotification
  tags: Testing
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/enterprisesenterpriseidsendtestpushnotification-post-openapi.md
- name: Google Play Return Service Account
  x-api-slug: google-play
  description: |-
    Returns a service account and credentials. The service account can be bound to the enterprise by calling setAccount. The service account is unique to this enterprise and EMM, and will be deleted if the enterprise is unbound. The credentials contain private key data and are not stored server-side.

    This method can only be called after calling Enterprises.Enroll or Enterprises.CompleteSignup, and before Enterprises.SetAccount; at other times it will return an error.

    Subsequent calls after the first will generate a new, unique set of credentials, and invalidate the previously generated credentials.

    Once the service account is bound to the enterprise, it can be managed using the serviceAccountKeys resource.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///enterprises/{enterpriseId}/serviceAccount
  tags: Account
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/enterprisesenterpriseidserviceaccount-get-openapi.md
- name: Google Play Delete In App Products
  x-api-slug: google-play
  description: Delete an in-app product for an app.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///{packageName}/inappproducts/{sku}
  tags: In App Product
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/packagenameinappproductssku-delete-openapi.md
- name: Google Play Return Active Credentials
  x-api-slug: google-play
  description: Lists all active credentials for the service account associated with
    this enterprise. Only the ID and key type are returned. The calling service account
    must have been retrieved by calling Enterprises.GetServiceAccount and must have
    been set as the enterprise service account by calling Enterprises.SetAccount.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///enterprises/{enterpriseId}/serviceAccountKeys
  tags: Credential
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/enterprisesenterpriseidserviceaccountkeys-get-openapi.md
- name: Google Play Get In App Product
  x-api-slug: google-play
  description: Returns information about the in-app product specified.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///{packageName}/inappproducts/{sku}
  tags: In App Product
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/packagenameinappproductssku-get-openapi.md
- name: Google Play Generate New Credentials
  x-api-slug: google-play
  description: |-
    Generates new credentials for the service account associated with this enterprise. The calling service account must have been retrieved by calling Enterprises.GetServiceAccount and must have been set as the enterprise service account by calling Enterprises.SetAccount.

    Only the type of the key should be populated in the resource to be inserted.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///enterprises/{enterpriseId}/serviceAccountKeys
  tags: Credential
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/enterprisesenterpriseidserviceaccountkeys-post-openapi.md
- name: Google Play Update In App Product
  x-api-slug: google-play
  description: Updates the details of an in-app product. This method supports patch
    semantics.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///{packageName}/inappproducts/{sku}
  tags: In App Product
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/packagenameinappproductssku-patch-openapi.md
- name: Google Play Remove and Invalidates Credentials
  x-api-slug: google-play
  description: Removes and invalidates the specified credentials for the service account
    associated with this enterprise. The calling service account must have been retrieved
    by calling Enterprises.GetServiceAccount and must have been set as the enterprise
    service account by calling Enterprises.SetAccount.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///enterprises/{enterpriseId}/serviceAccountKeys/{keyId}
  tags: Credential
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/enterprisesenterpriseidserviceaccountkeyskeyid-delete-openapi.md
- name: Google Play Get Store Layout
  x-api-slug: google-play
  description: Returns the store layout for the enterprise. If the store layout has
    not been set, or if the store layout has no homepageId set, returns a NOT_FOUND
    error.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///enterprises/{enterpriseId}/storeLayout
  tags: Store Layout
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/enterprisesenterpriseidstorelayout-get-openapi.md
- name: Google Play Update In App Product
  x-api-slug: google-play
  description: Updates the details of an in-app product.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///{packageName}/inappproducts/{sku}
  tags: In App Product
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/packagenameinappproductssku-put-openapi.md
- name: Google Play Update Store Layout
  x-api-slug: google-play
  description: Sets the store layout for the enterprise. By default, storeLayoutType
    is set to "basic" and the basic store layout is enabled. The basic layout only
    contains apps approved by the admin, and that have been added to the available
    product set for a user (using the  setAvailableProductSet call). Apps on the page
    are sorted in order of their product ID value. If you create a custom store layout
    (by setting storeLayoutType = "custom"), the basic store layout is disabled.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///enterprises/{enterpriseId}/storeLayout
  tags: Store Layout
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/enterprisesenterpriseidstorelayout-put-openapi.md
- name: Google Play Get Store Layout Pages
  x-api-slug: google-play
  description: Retrieves the details of all pages in the store.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///enterprises/{enterpriseId}/storeLayout/pages
  tags: Store Layout Page
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/enterprisesenterpriseidstorelayoutpages-get-openapi.md
- name: Google Play Create Store Layout Page
  x-api-slug: google-play
  description: Inserts a new store page.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///enterprises/{enterpriseId}/storeLayout/pages
  tags: Store Layout Page
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/enterprisesenterpriseidstorelayoutpages-post-openapi.md
- name: Google Play Get In App Purchases
  x-api-slug: google-play
  description: Checks the purchase and consumption status of an inapp item.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///{packageName}/purchases/products/{productId}/tokens/{token}
  tags: In App Purchase
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/packagenamepurchasesproductsproductidtokenstoken-get-openapi.md
- name: Google Play Delete Store Layout Page
  x-api-slug: google-play
  description: Deletes a store page.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///enterprises/{enterpriseId}/storeLayout/pages/{pageId}
  tags: Store Layout Page
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/enterprisesenterpriseidstorelayoutpagespageid-delete-openapi.md
- name: Google Play Check User Subscriptions
  x-api-slug: google-play
  description: Checks whether a user's subscription purchase is valid and returns
    its expiry time.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///{packageName}/purchases/subscriptions/{subscriptionId}/tokens/{token}
  tags: Subscription
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/packagenamepurchasessubscriptionssubscriptionidtokenstoken-get-openapi.md
- name: Google Play Get Store Layout Page
  x-api-slug: google-play
  description: Retrieves details of a store page.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///enterprises/{enterpriseId}/storeLayout/pages/{pageId}
  tags: Store Layout Page
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/enterprisesenterpriseidstorelayoutpagespageid-get-openapi.md
- name: Google Play Update Store Layout Page
  x-api-slug: google-play
  description: Updates the content of a store page. This method supports patch semantics.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///enterprises/{enterpriseId}/storeLayout/pages/{pageId}
  tags: Store Layout Page
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/enterprisesenterpriseidstorelayoutpagespageid-patch-openapi.md
- name: Google Play Cancel User Subscription
  x-api-slug: google-play
  description: Cancels a user's subscription purchase. The subscription remains valid
    until its expiration time.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///{packageName}/purchases/subscriptions/{subscriptionId}/tokens/{token}:cancel
  tags: Subscription
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/packagenamepurchasessubscriptionssubscriptionidtokenstokencancel-post-openapi.md
- name: Google Play Create Store Layout Page
  x-api-slug: google-play
  description: Updates the content of a store page.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///enterprises/{enterpriseId}/storeLayout/pages/{pageId}
  tags: Store Layout Page Cluster
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/enterprisesenterpriseidstorelayoutpagespageid-put-openapi.md
- name: Google Play Defer User Subscription
  x-api-slug: google-play
  description: Defers a user's subscription purchase until a specified future expiration
    time.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///{packageName}/purchases/subscriptions/{subscriptionId}/tokens/{token}:defer
  tags: Subscription
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/packagenamepurchasessubscriptionssubscriptionidtokenstokendefer-post-openapi.md
- name: Google Play Get Store Layout Page Clusters
  x-api-slug: google-play
  description: Retrieves the details of all clusters on the specified page.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///enterprises/{enterpriseId}/storeLayout/pages/{pageId}/clusters
  tags: Store Layout Page Cluster
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/enterprisesenterpriseidstorelayoutpagespageidclusters-get-openapi.md
- name: Google Play Refund User Subscription
  x-api-slug: google-play
  description: Refunds a user's subscription purchase, but the subscription remains
    valid until its expiration time and it will continue to recur.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///{packageName}/purchases/subscriptions/{subscriptionId}/tokens/{token}:refund
  tags: Subscription
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/packagenamepurchasessubscriptionssubscriptionidtokenstokenrefund-post-openapi.md
- name: Google Play Insert Store Layout Page Cluster
  x-api-slug: google-play
  description: Inserts a new cluster in a page.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///enterprises/{enterpriseId}/storeLayout/pages/{pageId}/clusters
  tags: Store Layout Page Cluster
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/enterprisesenterpriseidstorelayoutpagespageidclusters-post-openapi.md
- name: Google Play Delete Store Layout Page Cluster
  x-api-slug: google-play
  description: Deletes a cluster.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///enterprises/{enterpriseId}/storeLayout/pages/{pageId}/clusters/{clusterId}
  tags: Store Layout Page Cluster
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/enterprisesenterpriseidstorelayoutpagespageidclustersclusterid-delete-openapi.md
- name: Google Play Refunds and Revoke
  x-api-slug: google-play
  description: Refunds and immediately revokes a user's subscription purchase. Access
    to the subscription will be terminated immediately and it will stop recurring.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///{packageName}/purchases/subscriptions/{subscriptionId}/tokens/{token}:revoke
  tags: Subscription
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/packagenamepurchasessubscriptionssubscriptionidtokenstokenrevoke-post-openapi.md
- name: Google Play Get Store Layout Page Cluster
  x-api-slug: google-play
  description: Retrieves details of a cluster.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///enterprises/{enterpriseId}/storeLayout/pages/{pageId}/clusters/{clusterId}
  tags: Store Layout Page Cluster
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/enterprisesenterpriseidstorelayoutpagespageidclustersclusterid-get-openapi.md
- name: Google Play List Cancelled Purches
  x-api-slug: google-play
  description: Lists the purchases that were cancelled, refunded or charged-back.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///{packageName}/purchases/voidedpurchases
  tags: Subscription
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/packagenamepurchasesvoidedpurchases-get-openapi.md
- name: Google Play Update Store Layout Page Cluster
  x-api-slug: google-play
  description: Updates a cluster. This method supports patch semantics.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///enterprises/{enterpriseId}/storeLayout/pages/{pageId}/clusters/{clusterId}
  tags: Store Layout Page Cluster
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/enterprisesenterpriseidstorelayoutpagespageidclustersclusterid-patch-openapi.md
- name: Google Play Get Reviews
  x-api-slug: google-play
  description: Returns a list of reviews. Only reviews from last week will be returned.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///{packageName}/reviews
  tags: Reviews
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/packagenamereviews-get-openapi.md
- name: Google Play Update Store Layout Page Cluster
  x-api-slug: google-play
  description: Updates a cluster.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///enterprises/{enterpriseId}/storeLayout/pages/{pageId}/clusters/{clusterId}
  tags: Store Layout Page Cluster
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/enterprisesenterpriseidstorelayoutpagespageidclustersclusterid-put-openapi.md
- name: Google Play Unenroll Enterprise
  x-api-slug: google-play
  description: Unenrolls an enterprise from the calling EMM.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///enterprises/{enterpriseId}/unenroll
  tags: Enterprise
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/enterprisesenterpriseidunenroll-post-openapi.md
- name: Google Play Get Review
  x-api-slug: google-play
  description: Returns a single review.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///{packageName}/reviews/{reviewId}
  tags: Reviews
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/packagenamereviewsreviewid-get-openapi.md
- name: Google Play Lookup User
  x-api-slug: google-play
  description: Looks up a user by primary email address. This is only supported for
    Google-managed users. Lookup of the id is not needed for EMM-managed users because
    the id is already returned in the result of the Users.insert call.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///enterprises/{enterpriseId}/users
  tags: User
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/enterprisesenterpriseidusers-get-openapi.md
- name: Google Play Reply To Review
  x-api-slug: google-play
  description: Reply to a single review, or update an existing reply.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///{packageName}/reviews/{reviewId}:reply
  tags: Reviews
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/packagenamereviewsreviewidreply-post-openapi.md
- name: Google Play Create New User
  x-api-slug: google-play
  description: |-
    Creates a new EMM-managed user.

    The Users resource passed in the body of the request should include an accountIdentifier and an accountType.
    If a corresponding user already exists with the same account identifier, the user will be updated with the resource. In this case only the displayName field can be changed.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///enterprises/{enterpriseId}/users
  tags: User
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/enterprisesenterpriseidusers-post-openapi.md
- name: Google Play Delete User
  x-api-slug: google-play
  description: Deleted an EMM-managed user.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///enterprises/{enterpriseId}/users/{userId}
  tags: User
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/enterprisesenterpriseidusersuserid-delete-openapi.md
- name: Google Play Get User
  x-api-slug: google-play
  description: Retrieves a user's details.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///enterprises/{enterpriseId}/users/{userId}
  tags: User
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/enterprisesenterpriseidusersuserid-get-openapi.md
- name: Google Play Update User
  x-api-slug: google-play
  description: |-
    Updates the details of an EMM-managed user.

    Can be used with EMM-managed users only (not Google managed users). Pass the new details in the Users resource in the request body. Only the displayName field can be changed. Other fields must either be unset or have the currently active value. This method supports patch semantics.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///enterprises/{enterpriseId}/users/{userId}
  tags: User
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/enterprisesenterpriseidusersuserid-patch-openapi.md
- name: Google Play Update User
  x-api-slug: google-play
  description: |-
    Updates the details of an EMM-managed user.

    Can be used with EMM-managed users only (not Google managed users). Pass the new details in the Users resource in the request body. Only the displayName field can be changed. Other fields must either be unset or have the currently active value.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///enterprises/{enterpriseId}/users/{userId}
  tags: User
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/enterprisesenterpriseidusersuserid-put-openapi.md
- name: Google Play Generate Authentication Token
  x-api-slug: google-play
  description: |-
    Generates an authentication token which the device policy client can use to provision the given EMM-managed user account on a device. The generated token is single-use and expires after a few minutes.

    This call only works with EMM-managed accounts.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///enterprises/{enterpriseId}/users/{userId}/authenticationToken
  tags: Token
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/enterprisesenterpriseidusersuseridauthenticationtoken-post-openapi.md
- name: Google Play Get Products
  x-api-slug: google-play
  description: Retrieves the set of products a user is entitled to access.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///enterprises/{enterpriseId}/users/{userId}/availableProductSet
  tags: Product
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/enterprisesenterpriseidusersuseridavailableproductset-get-openapi.md
- name: Google Play Update Products
  x-api-slug: google-play
  description: Modifies the set of products that a user is entitled to access (referred
    to as whitelisted products). Only products that are approved or products that
    were previously approved (products with revoked approval) can be whitelisted.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///enterprises/{enterpriseId}/users/{userId}/availableProductSet
  tags: Product
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/enterprisesenterpriseidusersuseridavailableproductset-put-openapi.md
- name: Google Play Get User Devices
  x-api-slug: google-play
  description: Retrieves the IDs of all of a user's devices.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///enterprises/{enterpriseId}/users/{userId}/devices
  tags: Device
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/enterprisesenterpriseidusersuseriddevices-get-openapi.md
- name: Google Play Get User Device
  x-api-slug: google-play
  description: Retrieves the details of a device.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///enterprises/{enterpriseId}/users/{userId}/devices/{deviceId}
  tags: Device
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/enterprisesenterpriseidusersuseriddevicesdeviceid-get-openapi.md
- name: Google Play Get App Installs
  x-api-slug: google-play
  description: Retrieves the details of all apps installed on the specified device.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///enterprises/{enterpriseId}/users/{userId}/devices/{deviceId}/installs
  tags: App Install
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/enterprisesenterpriseidusersuseriddevicesdeviceidinstalls-get-openapi.md
- name: Google Play Remove App Install
  x-api-slug: google-play
  description: Requests to remove an app from a device. A call to get or list will
    still show the app as installed on the device until it is actually removed.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///enterprises/{enterpriseId}/users/{userId}/devices/{deviceId}/installs/{installId}
  tags: App Install
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/enterprisesenterpriseidusersuseriddevicesdeviceidinstallsinstallid-delete-openapi.md
- name: Google Play Get App Install
  x-api-slug: google-play
  description: Retrieves details of an installation of an app on a device.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///enterprises/{enterpriseId}/users/{userId}/devices/{deviceId}/installs/{installId}
  tags: App Install
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/enterprisesenterpriseidusersuseriddevicesdeviceidinstallsinstallid-get-openapi.md
- name: Google Play Update App Install
  x-api-slug: google-play
  description: Requests to install the latest version of an app to a device. If the
    app is already installed, then it is updated to the latest version if necessary.
    This method supports patch semantics.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///enterprises/{enterpriseId}/users/{userId}/devices/{deviceId}/installs/{installId}
  tags: App Install
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/enterprisesenterpriseidusersuseriddevicesdeviceidinstallsinstallid-patch-openapi.md
- name: Google Play Update App Install
  x-api-slug: google-play
  description: Requests to install the latest version of an app to a device. If the
    app is already installed, then it is updated to the latest version if necessary.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///enterprises/{enterpriseId}/users/{userId}/devices/{deviceId}/installs/{installId}
  tags: App Install
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/enterprisesenterpriseidusersuseriddevicesdeviceidinstallsinstallid-put-openapi.md
- name: Google Play Get Per Device App Installs
  x-api-slug: google-play
  description: Lists all the per-device managed configurations for the specified device.
    Only the ID is set.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///enterprises/{enterpriseId}/users/{userId}/devices/{deviceId}/managedConfigurationsForDevice
  tags: App Install
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/enterprisesenterpriseidusersuseriddevicesdeviceidmanagedconfigurationsfordevice-get-openapi.md
- name: Google Play Remove Per Device App Install
  x-api-slug: google-play
  description: Removes a per-device managed configuration for an app for the specified
    device.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///enterprises/{enterpriseId}/users/{userId}/devices/{deviceId}/managedConfigurationsForDevice/{managedConfigurationForDeviceId}
  tags: App Install
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/enterprisesenterpriseidusersuseriddevicesdeviceidmanagedconfigurationsfordevicemanagedconfigurationfordeviceid-delete-openapi.md
- name: Google Play Get Per Device App Install
  x-api-slug: google-play
  description: Retrieves details of a per-device managed configuration.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///enterprises/{enterpriseId}/users/{userId}/devices/{deviceId}/managedConfigurationsForDevice/{managedConfigurationForDeviceId}
  tags: App Install
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/enterprisesenterpriseidusersuseriddevicesdeviceidmanagedconfigurationsfordevicemanagedconfigurationfordeviceid-get-openapi.md
- name: Google Play Update Per Device App Install
  x-api-slug: google-play
  description: Adds or updates a per-device managed configuration for an app for the
    specified device. This method supports patch semantics.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///enterprises/{enterpriseId}/users/{userId}/devices/{deviceId}/managedConfigurationsForDevice/{managedConfigurationForDeviceId}
  tags: App Install
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/enterprisesenterpriseidusersuseriddevicesdeviceidmanagedconfigurationsfordevicemanagedconfigurationfordeviceid-patch-openapi.md
- name: Google Play Update Per Device App Install
  x-api-slug: google-play
  description: Adds or updates a per-device managed configuration for an app for the
    specified device.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///enterprises/{enterpriseId}/users/{userId}/devices/{deviceId}/managedConfigurationsForDevice/{managedConfigurationForDeviceId}
  tags: App Install
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/enterprisesenterpriseidusersuseriddevicesdeviceidmanagedconfigurationsfordevicemanagedconfigurationfordeviceid-put-openapi.md
- name: Google Play Get Per Device App Install State
  x-api-slug: google-play
  description: Retrieves whether a device's access to Google services is enabled or
    disabled. The device state takes effect only if enforcing EMM policies on Android
    devices is enabled in the Google Admin Console. Otherwise, the device state is
    ignored and all devices are allowed access to Google services. This is only supported
    for Google-managed users.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///enterprises/{enterpriseId}/users/{userId}/devices/{deviceId}/state
  tags: App Install
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/enterprisesenterpriseidusersuseriddevicesdeviceidstate-get-openapi.md
- name: Google Play Update Per Device App Install State
  x-api-slug: google-play
  description: Sets whether a device's access to Google services is enabled or disabled.
    The device state takes effect only if enforcing EMM policies on Android devices
    is enabled in the Google Admin Console. Otherwise, the device state is ignored
    and all devices are allowed access to Google services. This is only supported
    for Google-managed users.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///enterprises/{enterpriseId}/users/{userId}/devices/{deviceId}/state
  tags: App Install
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/enterprisesenterpriseidusersuseriddevicesdeviceidstate-put-openapi.md
- name: Google Play Get Entitlements
  x-api-slug: google-play
  description: Lists all entitlements for the specified user. Only the ID is set.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///enterprises/{enterpriseId}/users/{userId}/entitlements
  tags: Entitlement
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/enterprisesenterpriseidusersuseridentitlements-get-openapi.md
- name: Google Play Remove Entitlement
  x-api-slug: google-play
  description: Removes an entitlement to an app for a user.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///enterprises/{enterpriseId}/users/{userId}/entitlements/{entitlementId}
  tags: Entitlement
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/enterprisesenterpriseidusersuseridentitlementsentitlementid-delete-openapi.md
- name: Google Play Get Entitlement
  x-api-slug: google-play
  description: Retrieves details of an entitlement.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///enterprises/{enterpriseId}/users/{userId}/entitlements/{entitlementId}
  tags: Entitlement
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/enterprisesenterpriseidusersuseridentitlementsentitlementid-get-openapi.md
- name: Google Play Update Entitlement
  x-api-slug: google-play
  description: Adds or updates an entitlement to an app for a user. This method supports
    patch semantics.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///enterprises/{enterpriseId}/users/{userId}/entitlements/{entitlementId}
  tags: Entitlement
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/enterprisesenterpriseidusersuseridentitlementsentitlementid-patch-openapi.md
- name: Google Play Update Entitlement
  x-api-slug: google-play
  description: Adds or updates an entitlement to an app for a user.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///enterprises/{enterpriseId}/users/{userId}/entitlements/{entitlementId}
  tags: Entitlement
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/enterprisesenterpriseidusersuseridentitlementsentitlementid-put-openapi.md
- name: Google Play Get Per User Configurations
  x-api-slug: google-play
  description: Lists all the per-user managed configurations for the specified user.
    Only the ID is set.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///enterprises/{enterpriseId}/users/{userId}/managedConfigurationsForUser
  tags: Configuration
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/enterprisesenterpriseidusersuseridmanagedconfigurationsforuser-get-openapi.md
- name: Google Play Delete Per User Configurations
  x-api-slug: google-play
  description: Removes a per-user managed configuration for an app for the specified
    user.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///enterprises/{enterpriseId}/users/{userId}/managedConfigurationsForUser/{managedConfigurationForUserId}
  tags: Configuration
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/enterprisesenterpriseidusersuseridmanagedconfigurationsforusermanagedconfigurationforuserid-delete-openapi.md
- name: Google Play Get Per User Configuration
  x-api-slug: google-play
  description: Retrieves details of a per-user managed configuration for an app for
    the specified user.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///enterprises/{enterpriseId}/users/{userId}/managedConfigurationsForUser/{managedConfigurationForUserId}
  tags: Configuration
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/enterprisesenterpriseidusersuseridmanagedconfigurationsforusermanagedconfigurationforuserid-get-openapi.md
- name: Google Play Update Per User Configuration
  x-api-slug: google-play
  description: Adds or updates a per-user managed configuration for an app for the
    specified user. This method supports patch semantics.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///enterprises/{enterpriseId}/users/{userId}/managedConfigurationsForUser/{managedConfigurationForUserId}
  tags: Configuration
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/enterprisesenterpriseidusersuseridmanagedconfigurationsforusermanagedconfigurationforuserid-patch-openapi.md
- name: Google Play Update Per User Configuration
  x-api-slug: google-play
  description: Adds or updates a per-user managed configuration for an app for the
    specified user.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///enterprises/{enterpriseId}/users/{userId}/managedConfigurationsForUser/{managedConfigurationForUserId}
  tags: Configuration
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/enterprisesenterpriseidusersuseridmanagedconfigurationsforusermanagedconfigurationforuserid-put-openapi.md
- name: Google Play Delete User Token
  x-api-slug: google-play
  description: Revokes a previously generated token (activation code) for the user.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///enterprises/{enterpriseId}/users/{userId}/token
  tags: Token
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/enterprisesenterpriseidusersuseridtoken-delete-openapi.md
- name: Google Play Generate User Token
  x-api-slug: google-play
  description: |-
    Generates a token (activation code) to allow this user to configure their managed account in the Android Setup Wizard. Revokes any previously generated token.

    This call only works with Google managed accounts.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///enterprises/{enterpriseId}/users/{userId}/token
  tags: Token
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/enterprisesenterpriseidusersuseridtoken-post-openapi.md
- name: Google Play Get Permissions
  x-api-slug: google-play
  description: Retrieves details of an Android app permission for display to an enterprise
    admin.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///permissions/{permissionId}
  tags: Permission
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/permissionspermissionid-get-openapi.md
- name: Google Play Get State Keys
  x-api-slug: google-play
  description: Lists all the states keys, and optionally the state data.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///states
  tags: Application State
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/states-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/states-get-openapi.md
- name: Google Play Delete State Key
  x-api-slug: google-play
  description: Deletes a key and the data associated with it. The key is removed and
    no longer counts against the key quota. Note that since this method is not safe
    in the face of concurrent modifications, it should only be used for development
    and testing purposes. Invoking this method in shipping code can result in data
    loss and data corruption.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///states/{stateKey}
  tags: Application State
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/statesstatekey-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/statesstatekey-delete-openapi.md
- name: Google Play Get State Key
  x-api-slug: google-play
  description: Retrieves the data corresponding to the passed key. If the key does
    not exist on the server, an HTTP 404 will be returned.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///states/{stateKey}
  tags: Application State
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/statesstatekey-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/statesstatekey-get-openapi.md
- name: Google Play Update State Key
  x-api-slug: google-play
  description: Update the data associated with the input key if and only if the passed
    version matches the currently stored version. This method is safe in the face
    of concurrent writes. Maximum per-key size is 128KB.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///states/{stateKey}
  tags: Application State
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/statesstatekey-put-openapi.md
- name: Google Play Clear State Key
  x-api-slug: google-play
  description: Clears (sets to empty) the data for the passed key if and only if the
    passed version matches the currently stored version. This method results in a
    conflict error on version mismatch.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///states/{stateKey}/clear
  tags: Application State
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/statesstatekeyclear-post-openapi.md
- name: Google Play Get Achievements
  x-api-slug: google-play
  description: Lists all the achievement definitions for your application.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///achievements
  tags: Achievement
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/achievements-get-openapi.md
- name: Google Play Update Multiple Achievements
  x-api-slug: google-play
  description: Updates multiple achievements for the currently authenticated player.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///achievements/updateMultiple
  tags: Achievement
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/achievementsupdatemultiple-post-openapi.md
- name: Google Play Increment Step Of Achievement
  x-api-slug: google-play
  description: Increments the steps of the achievement with the given ID for the currently
    authenticated player.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///achievements/{achievementId}/increment
  tags: Achievement
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/achievementsachievementidincrement-post-openapi.md
- name: Google Play Set State of Achievement
  x-api-slug: google-play
  description: Sets the state of the achievement with the given ID to REVEALED for
    the currently authenticated player.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///achievements/{achievementId}/reveal
  tags: Achievement
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/achievementsachievementidreveal-post-openapi.md
- name: Google Play Set Steps for Achievements
  x-api-slug: google-play
  description: Sets the steps for the currently authenticated player towards unlocking
    an achievement. If the steps parameter is less than the current number of steps
    that the player already gained for the achievement, the achievement is not modified.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///achievements/{achievementId}/setStepsAtLeast
  tags: Achievement
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/achievementsachievementidsetstepsatleast-post-openapi.md
- name: Google Play Unlock Achievement
  x-api-slug: google-play
  description: Unlocks this achievement for the currently authenticated player.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///achievements/{achievementId}/unlock
  tags: Achievement
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/achievementsachievementidunlock-post-openapi.md
- name: Google Play Set Played
  x-api-slug: google-play
  description: Indicate that the the currently authenticated user is playing your
    application.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///applications/played
  tags: Application
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/applicationsplayed-post-openapi.md
- name: Google Play Get Application
  x-api-slug: google-play
  description: Retrieves the metadata of the application with the given ID. If the
    requested application is not available for the specified platformType, the returned
    response will not include any instance data.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///applications/{applicationId}
  tags: Application
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/applicationsapplicationid-get-openapi.md
- name: Google Play Verify Token
  x-api-slug: google-play
  description: Verifies the auth token provided with this request is for the application
    with the specified ID, and returns the ID of the player it was granted for.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///applications/{applicationId}/verify
  tags: Token
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/applicationsapplicationidverify-get-openapi.md
- name: Google Play Get Event Definitions
  x-api-slug: google-play
  description: Returns a list of the event definitions in this application.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///eventDefinitions
  tags: Event
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/eventdefinitions-get-openapi.md
- name: Google Play Get Events
  x-api-slug: google-play
  description: Returns a list showing the current progress on events in this application
    for the currently authenticated user.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///events
  tags: Event
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/events-get-openapi.md
- name: Google Play Create Event
  x-api-slug: google-play
  description: Records a batch of changes to the number of times events have occurred
    for the currently authenticated user of this application.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///events
  tags: Event
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/events-post-openapi.md
- name: Google Play Get Leader Boards
  x-api-slug: google-play
  description: Lists all the leaderboard metadata for your application.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///leaderboards
  tags: Leader Board
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/leaderboards-get-openapi.md
- name: Google Play Create Leader Board
  x-api-slug: google-play
  description: Submits multiple scores to leaderboards.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///leaderboards/scores
  tags: Leader Board
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/leaderboardsscores-post-openapi.md
- name: Google Play Get Leader Board
  x-api-slug: google-play
  description: Retrieves the metadata of the leaderboard with the given ID.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///leaderboards/{leaderboardId}
  tags: Leader Board
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/leaderboardsleaderboardid-get-openapi.md
- name: Google Play Update Leader Board Score
  x-api-slug: google-play
  description: Submits a score to the specified leaderboard.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///leaderboards/{leaderboardId}/scores
  tags: Leader Board
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/leaderboardsleaderboardidscores-post-openapi.md
- name: Google Play Get Leader Board Scores
  x-api-slug: google-play
  description: Lists the scores in a leaderboard, starting from the top.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///leaderboards/{leaderboardId}/scores/{collection}
  tags: Leader Board
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/leaderboardsleaderboardidscorescollection-get-openapi.md
- name: Google Play Get Leader Board Window
  x-api-slug: google-play
  description: Lists the scores in a leaderboard around (and including) a player's
    score.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///leaderboards/{leaderboardId}/window/{collection}
  tags: Leader Board
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/leaderboardsleaderboardidwindowcollection-get-openapi.md
- name: Google Play Get Metagame Confirmation
  x-api-slug: google-play
  description: Return the metagame configuration data for the calling application.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///metagameConfig
  tags: Game
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/metagameconfig-get-openapi.md
- name: Google Play Get PLayers
  x-api-slug: google-play
  description: Get the collection of players for the currently authenticated user.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///players/me/players/{collection}
  tags: Player
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/playersmeplayerscollection-get-openapi.md
- name: Google Play Get Player
  x-api-slug: google-play
  description: Retrieves the Player resource with the given ID. To retrieve the player
    for the currently authenticated user, set playerId to me.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///players/{playerId}
  tags: Player
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/playersplayerid-get-openapi.md
- name: Google Play Get Player Achievements
  x-api-slug: google-play
  description: Lists the progress for all your application's achievements for the
    currently authenticated player.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///players/{playerId}/achievements
  tags: Player
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/playersplayeridachievements-get-openapi.md
- name: Google Play Get Player Categories
  x-api-slug: google-play
  description: List play data aggregated per category for the player corresponding
    to playerId.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///players/{playerId}/categories/{collection}
  tags: Player
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/playersplayeridcategoriescollection-get-openapi.md
- name: Google Play Get Player Leaderboard Scores
  x-api-slug: google-play
  description: |-
    Get high scores, and optionally ranks, in leaderboards for the currently authenticated player. For a specific time span, leaderboardId can be set to ALL to retrieve data for all leaderboards in a given time span.
    NOTE: You cannot ask for 'ALL' leaderboards and 'ALL' timeSpans in the same request; only one parameter may be set to 'ALL'.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///players/{playerId}/leaderboards/{leaderboardId}/scores/{timeSpan}
  tags: Player
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/playersplayeridleaderboardsleaderboardidscorestimespan-get-openapi.md
- name: Google Play Get Guests
  x-api-slug: google-play
  description: Get a list of quests for your application and the currently authenticated
    player.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///players/{playerId}/quests
  tags: Guest
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/playersplayeridquests-get-openapi.md
- name: Google Play Get Player Snapshots
  x-api-slug: google-play
  description: Retrieves a list of snapshots created by your application for the player
    corresponding to the player ID.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///players/{playerId}/snapshots
  tags: Player
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/playersplayeridsnapshots-get-openapi.md
- name: Google Play Register Push Token
  x-api-slug: google-play
  description: Registers a push token for the current user and application.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///pushtokens
  tags: Token
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/pushtokens-put-openapi.md
- name: Google Play Remove Push Token
  x-api-slug: google-play
  description: Removes a push token for the current user and application. Removing
    a non-existent push token will report success.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///pushtokens/remove
  tags: Token
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/pushtokensremove-post-openapi.md
- name: Google Play Accept Quest
  x-api-slug: google-play
  description: Indicates that the currently authorized user will participate in the
    quest.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///quests/{questId}/accept
  tags: Quest
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/questsquestidaccept-post-openapi.md
- name: Google Play Claim Quest Milestone
  x-api-slug: google-play
  description: Report that a reward for the milestone corresponding to milestoneId
    for the quest corresponding to questId has been claimed by the currently authorized
    user.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///quests/{questId}/milestones/{milestoneId}/claim
  tags: Milestone
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/questsquestidmilestonesmilestoneidclaim-put-openapi.md
- name: Google Play Check Revision
  x-api-slug: google-play
  description: Checks whether the games client is out of date.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///revisions/check
  tags: Revision
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/revisionscheck-get-openapi.md
- name: Google Play Get Rooms
  x-api-slug: google-play
  description: Returns invitations to join rooms.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///rooms
  tags: Room
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/rooms-get-openapi.md
- name: Google Play Create Room
  x-api-slug: google-play
  description: Create a room. For internal use by the Games SDK only. Calling this
    method directly is unsupported.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///rooms/create
  tags: Room
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/roomscreate-post-openapi.md
- name: Google Play Get Room
  x-api-slug: google-play
  description: Get the data for a room.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///rooms/{roomId}
  tags: Room
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/roomsroomid-get-openapi.md
- name: Google Play Decline Room
  x-api-slug: google-play
  description: Decline an invitation to join a room. For internal use by the Games
    SDK only. Calling this method directly is unsupported.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///rooms/{roomId}/decline
  tags: Room
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/roomsroomiddecline-post-openapi.md
- name: Google Play Dismiss Room
  x-api-slug: google-play
  description: Dismiss an invitation to join a room. For internal use by the Games
    SDK only. Calling this method directly is unsupported.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///rooms/{roomId}/dismiss
  tags: Room
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/roomsroomiddismiss-post-openapi.md
- name: Google Play Join Room
  x-api-slug: google-play
  description: Join a room. For internal use by the Games SDK only. Calling this method
    directly is unsupported.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///rooms/{roomId}/join
  tags: Room
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/roomsroomidjoin-post-openapi.md
- name: Google Play Leave Room
  x-api-slug: google-play
  description: Leave a room. For internal use by the Games SDK only. Calling this
    method directly is unsupported.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///rooms/{roomId}/leave
  tags: Room
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/roomsroomidleave-post-openapi.md
- name: Google Play Report Room Status
  x-api-slug: google-play
  description: Updates sent by a client reporting the status of peers in a room. For
    internal use by the Games SDK only. Calling this method directly is unsupported.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///rooms/{roomId}/reportstatus
  tags: Room
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/roomsroomidreportstatus-post-openapi.md
- name: Google Play Get Snapshot
  x-api-slug: google-play
  description: Retrieves the metadata for a given snapshot ID.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///snapshots/{snapshotId}
  tags: Snapshot
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/snapshotssnapshotid-get-openapi.md
- name: Google Play Return Turn-Based Match
  x-api-slug: google-play
  description: Returns turn-based matches the player is or was involved in.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///turnbasedmatches
  tags: Match
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/turnbasedmatches-get-openapi.md
- name: Google Play Create Turn-Based Match
  x-api-slug: google-play
  description: Create a turn-based match.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///turnbasedmatches/create
  tags: Match
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/turnbasedmatchescreate-post-openapi.md
- name: Google Play Sync Turn-Based Match
  x-api-slug: google-play
  description: Returns turn-based matches the player is or was involved in that changed
    since the last sync call, with the least recent changes coming first. Matches
    that should be removed from the local cache will have a status of MATCH_DELETED.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///turnbasedmatches/sync
  tags: Match
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/turnbasedmatchessync-get-openapi.md
- name: Google Play Get Turn-Based Match
  x-api-slug: google-play
  description: Get the data for a turn-based match.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///turnbasedmatches/{matchId}
  tags: Match
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/turnbasedmatchesmatchid-get-openapi.md
- name: Google Play Update Turn-Based Match
  x-api-slug: google-play
  description: Cancel a turn-based match.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///turnbasedmatches/{matchId}/cancel
  tags: Match
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/turnbasedmatchesmatchidcancel-put-openapi.md
- name: Google Play Decline Turn-Based Match
  x-api-slug: google-play
  description: Decline an invitation to play a turn-based match.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///turnbasedmatches/{matchId}/decline
  tags: Match
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/turnbasedmatchesmatchiddecline-put-openapi.md
- name: Google Play Dismiss Turn-Based Match
  x-api-slug: google-play
  description: Dismiss a turn-based match from the match list. The match will no longer
    show up in the list and will not generate notifications.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///turnbasedmatches/{matchId}/dismiss
  tags: Match
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/turnbasedmatchesmatchiddismiss-put-openapi.md
- name: Google Play Finish Turn-Based Match
  x-api-slug: google-play
  description: Finish a turn-based match. Each player should make this call once,
    after all results are in. Only the player whose turn it is may make the first
    call to Finish, and can pass in the final match state.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///turnbasedmatches/{matchId}/finish
  tags: Match
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/turnbasedmatchesmatchidfinish-put-openapi.md
- name: Google Play Join Turn-Based Match
  x-api-slug: google-play
  description: Join a turn-based match.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///turnbasedmatches/{matchId}/join
  tags: Match
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/turnbasedmatchesmatchidjoin-put-openapi.md
- name: Google Play Leave Turn-Based Match
  x-api-slug: google-play
  description: Leave a turn-based match when it is not the current player's turn,
    without canceling the match.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///turnbasedmatches/{matchId}/leave
  tags: Match
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/turnbasedmatchesmatchidleave-put-openapi.md
- name: Google Play ReLeave Turnturn Turn-Based Match
  x-api-slug: google-play
  description: Leave a turn-based match during the current player's turn, without
    canceling the match.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///turnbasedmatches/{matchId}/leaveTurn
  tags: Match
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/turnbasedmatchesmatchidleaveturn-put-openapi.md
- name: Google Play Rematch Turn-Based Match
  x-api-slug: google-play
  description: Create a rematch of a match that was previously completed, with the
    same participants. This can be called by only one player on a match still in their
    list; the player must have called Finish first. Returns the newly created match;
    it will be the caller's turn.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///turnbasedmatches/{matchId}/rematch
  tags: Match
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/turnbasedmatchesmatchidrematch-post-openapi.md
- name: Google Play Turn Turn-Based Match
  x-api-slug: google-play
  description: Commit the results of a player turn.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///turnbasedmatches/{matchId}/turn
  tags: Match
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/turnbasedmatchesmatchidturn-put-openapi.md
- name: Google Play Get Available Movies
  x-api-slug: google-play
  description: |-
    List Avails owned or managed by the partner.

    See _Authentication and Authorization rules_ and
    _List methods rules_ for more information about this method.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///v1/accounts/{accountId}/avails
  tags: Movie
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/v1accountsaccountidavails-get-openapi.md
- name: Google Play Get Available Movie
  x-api-slug: google-play
  description: Get an Avail given its avail group id and avail id.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///v1/accounts/{accountId}/avails/{availId}
  tags: Movie
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/v1accountsaccountidavailsavailid-get-openapi.md
- name: Google Play Get Orders
  x-api-slug: google-play
  description: |-
    List Orders owned or managed by the partner.

    See _Authentication and Authorization rules_ and
    _List methods rules_ for more information about this method.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///v1/accounts/{accountId}/orders
  tags: Order
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/v1accountsaccountidorders-get-openapi.md
- name: Google Play Get Order
  x-api-slug: google-play
  description: |-
    Get an Order given its id.

    See _Authentication and Authorization rules_ and
    _Get methods rules_ for more information about this method.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///v1/accounts/{accountId}/orders/{orderId}
  tags: Order
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/v1accountsaccountidordersorderid-get-openapi.md
- name: Google Play Get Store Information
  x-api-slug: google-play
  description: |-
    List StoreInfos owned or managed by the partner.

    See _Authentication and Authorization rules_ and
    _List methods rules_ for more information about this method.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///v1/accounts/{accountId}/storeInfos
  tags: Store
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/v1accountsaccountidstoreinfos-get-openapi.md
- name: Google Play Get Video Country
  x-api-slug: google-play
  description: |-
    Get a StoreInfo given its video id and country.

    See _Authentication and Authorization rules_ and
    _Get methods rules_ for more information about this method.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https://///v1/accounts/{accountId}/storeInfos/{videoId}/country/{country}
  tags: Country
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/v1accountsaccountidstoreinfosvideoidcountrycountry-get-openapi.md
- name: Google Play
  x-api-slug: google-play
  description: 'The Google Play Developer API allows you to perform a number of publishing
    and app-management tasks. It includes two components: The Subscriptions and In-App
    Purchases API lets you manage in-app purchases and subscriptions. The Publishing
    API lets you upload and publish apps, and perform other publishing-related tasks.'
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-play.png
  humanURL: https://play.google.com/store
  baseURL: https:///
  tags: Google Play
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-play/master/_listings/google-play/openapi.md
x-common:
- type: x-blog
  url: https://blog.google/products/google-play/
- type: x-blog-rss
  url: https://blog.google/products/google-play/rss
- type: x-developer
  url: https://developers.google.com/android-publisher/
- type: x-facebook
  url: https://www.facebook.com/GooglePlay
- type: x-getting-started
  url: https://developers.google.com/android-publisher/getting_started
- type: x-twitter
  url: https://twitter.com/GooglePlay
- type: x-website
  url: https://play.google.com/store
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---