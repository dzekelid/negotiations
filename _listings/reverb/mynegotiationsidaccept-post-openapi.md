---
swagger: "2.0"
x-collection-name: Reverb
x-complete: 0
info:
  title: Reverb Post My Negotiations Accept
  description: Post my negotiations accept.
  termsOfService: https://reverb.com/page/terms
  contact:
    name: Reverb API
    url: https://dev.reverb.com
    email: integrations@reverb.com
  version: "3.0"
host: api.reverb.com
basePath: /api
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /my/listings/negotiations:
    get:
      summary: Get My Listings Negotiations
      description: Get a list of active negotiations as a seller
      operationId: getMyListingsNegotiations
      x-api-path-slug: mylistingsnegotiations-get
      parameters:
      - in: query
        name: offset
      - in: query
        name: page
      - in: query
        name: per_page
      responses:
        200:
          description: OK
      tags:
      - My
      - Listings
      - Negotiations
  /my/negotiations/buying:
    get:
      summary: Get My Negotiations Buying
      description: Get a list of active negotiations as a buyer
      operationId: getMyNegotiationsBuying
      x-api-path-slug: mynegotiationsbuying-get
      parameters:
      - in: query
        name: offset
      - in: query
        name: page
      - in: query
        name: per_page
      responses:
        200:
          description: OK
      tags:
      - My
      - Negotiations
      - Buying
  /my/negotiations/{id}:
    get:
      summary: Get My Negotiations
      description: Get my negotiations.
      operationId: getMyNegotiations
      x-api-path-slug: mynegotiationsid-get
      parameters:
      - in: path
        name: id
      responses:
        200:
          description: OK
      tags:
      - My
      - Negotiations
      - Id
  /my/negotiations/{id}/accept:
    post:
      summary: Post My Negotiations Accept
      description: Post my negotiations accept.
      operationId: postMyNegotiationsAccept
      x-api-path-slug: mynegotiationsidaccept-post
      parameters:
      - in: body
        name: body
        description: the content of the request
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: id
      responses:
        200:
          description: OK
      tags:
      - My
      - Negotiations
      - Id
      - Accept
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