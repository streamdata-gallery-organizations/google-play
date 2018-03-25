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
  /v1/accounts/{accountId}/storeInfos:
    get:
      summary: Get Store Information
      description: List StoreInfos owned or managed by the partner
      operationId: playmoviespartner.accounts.storeInfos.list
      parameters:
      - in: path
        name: accountId
        description: REQUIRED
      - in: query
        name: countries
        description: |-
          Filter StoreInfos that match (case-insensitive) any of the given country
          codes, using the "ISO 3166-1 alpha-2" format (examples: "US", "us", "Us")
      - in: query
        name: mids
        description: Filter StoreInfos that match any of the given `mid`s
      - in: query
        name: name
        description: |-
          Filter that matches StoreInfos with a `name` or `show_name`
          that contains the given case-insensitive name
      - in: query
        name: pageSize
        description: See _List methods rules_ for info about this field
      - in: query
        name: pageToken
        description: See _List methods rules_ for info about this field
      - in: query
        name: pphNames
        description: See _List methods rules_ for info about this field
      - in: query
        name: seasonIds
        description: Filter StoreInfos that match any of the given `season_id`s
      - in: query
        name: studioNames
        description: See _List methods rules_ for info about this field
      - in: query
        name: videoId
        description: Filter StoreInfos that match a given `video_id`
      - in: query
        name: videoIds
        description: Filter StoreInfos that match any of the given `video_id`s
      responses:
        200:
          description: OK
      tags:
      - store
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