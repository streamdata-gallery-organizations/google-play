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
  /enterprises/{enterpriseId}/products:
    get:
      summary: Get Products
      description: Finds approved products that match a query, or all approved products
        if there is no query
      operationId: androidenterprise.products.list
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
        description: The BCP47 tag for the user's preferred language (e
      - in: query
        name: maxResults
        description: Specifies the maximum number of products that can be returned
          per request
      - in: query
        name: query
        description: The search query as typed in the Google Play store search box
      - in: query
        name: token
        description: A pagination token is contained in a request''s response when
          there are more products
      responses:
        200:
          description: OK
      tags:
      - product
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