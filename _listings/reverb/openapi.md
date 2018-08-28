swagger: "2.0"
x-collection-name: Reverb
x-complete: 1
info:
  title: reverb
  description: reverb
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
  /my/negotiations/{id}/counter:
    post:
      summary: Post My Negotiations Counter
      description: Post my negotiations counter.
      operationId: postMyNegotiationsCounter
      x-api-path-slug: mynegotiationsidcounter-post
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
      - Counter
  /my/negotiations/{id}/decline:
    post:
      summary: Post My Negotiations Decline
      description: Post my negotiations decline.
      operationId: postMyNegotiationsDecline
      x-api-path-slug: mynegotiationsiddecline-post
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
      - Decline
  /listings/{id}/negotiation:
    get:
      summary: Get Listings Negotiation
      description: Returns the latest negotiation for the requesting user given a
        listing id
      operationId: getListingsNegotiation
      x-api-path-slug: listingsidnegotiation-get
      parameters:
      - in: path
        name: id
      responses:
        200:
          description: OK
      tags:
      - Listings
      - Id
      - Negotiation