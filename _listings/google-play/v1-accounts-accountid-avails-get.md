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
  /v1/accounts/{accountId}/avails:
    get:
      summary: Get Available Movies
      description: List Avails owned or managed by the partner
      operationId: playmoviespartner.accounts.avails.list
      parameters:
      - in: path
        name: accountId
        description: REQUIRED
      - in: query
        name: altId
        description: Filter Avails that match a case-insensitive, partner-specific
          custom id
      - in: query
        name: altIds
        description: Filter Avails that match (case-insensitive) any of the given
          partner-specific custom ids
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
        name: studioNames
        description: See _List methods rules_ for info about this field
      - in: query
        name: territories
        description: |-
          Filter Avails that match (case-insensitive) any of the given country codes,
          using the "ISO 3166-1 alpha-2" format (examples: "US", "us", "Us")
      - in: query
        name: title
        description: |-
          Filter that matches Avails with a `title_internal_alias`,
          `series_title_internal_alias`, `season_title_internal_alias`,
          or `episode_title_internal_alias` that contains the given
          case-insensitive title
      - in: query
        name: videoIds
        description: Filter Avails that match any of the given `video_id`s
      responses:
        200:
          description: OK
      tags:
      - movie
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