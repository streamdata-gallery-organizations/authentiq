---
swagger: "2.0"
x-collection-name: Authentiq Connect
x-complete: 0
info:
  title: Authentiq Connect Retrieve their user profile
  description: |-
    Use this endpoint to retrieve a user's profile in case you've not already obtained enough details from the ID Token via the Token Endpoint.
     See also:
     - [OIDC UserInfo endpoint](http://openid.net/specs/openid-connect-core-1_0.html#UserInfo)
  termsOfService: https://www.authentiq.com/tos/
  contact:
    name: Team Authentiq
    url: https://www.authentiq.com/
    email: hello@authentiq.com
  version: "1.0"
host: connect.authentiq.io
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /authorize:
    get:
      summary: Authenticate a user
      description: |-
        Start a session with Authentiq Connect and authenticate a user.

        Example:

        ```
        GET https://connect.authentiq.io/authorize?client_id=<your-client-id>&response_type=code+id_token&scope=openid+email&redirect_uri=<your-redirect-uri>&state=0123456789
        ```

        This endpoint is compatible with OpenID Connect and also supports the POST method, in which case the parameters are passed as a form post.

        See also:
          - [OAuth 2.0 Authorization Endpoint](http://tools.ietf.org/html/rfc6749#section-3.1)
          - [OIDC Authentication request](http://openid.net/specs/openid-connect-core-1_0.html#AuthRequest)
          - [OIDC Successful Authentication response](http://openid.net/specs/openid-connect-core-1_0.html#AuthResponse)
          - [OIDC Error Authentication response](http://openid.net/specs/openid-connect-core-1_0.html#AuthError)
      operationId: authorize
      x-api-path-slug: authorize-get
      parameters:
      - in: query
        name: client_id
        description: A client ID obtained from the [Dashboard](https://dashboard
      - in: query
        name: display
        description: The authentication display mode, which can be one of `page`,
          `popup` or `modal`
      - in: query
        name: max_age
        description: Specifies the allowable elapsed time in seconds since the last
          time the end-user was actively authenticated
      - in: query
        name: nonce
        description: An nonce provided by the client (and opaque to Authentiq Connect)
          that will be included in any ID Token generated for this session
      - in: query
        name: prompt
        description: Space-delimited, case sensitive list of ASCII string values that
          specifies whether the Authorization Server prompts the End-User for reauthentication
          and consent
      - in: query
        name: redirect_uri
        description: The location to redirect to after (un)successful authentication
      - in: query
        name: response_mode
        description: Whether to append parameters to the redirect URL in the query
          string (`query`) or as fragments (`fragment`)
      - in: query
        name: response_type
        description: The OIDC response type to use for this authentication flow
      - in: query
        name: scope
        description: The space-separated identity claims to request from the end-user
      - in: query
        name: state
        description: An opaque string that will be passed back to the redirect URL
          and therefore can be used to communicate client side state and prevent CSRF
          attacks
      - in: query
        name: ui_locales
        description: Specifies the preferred language to use on the authorization
          page, as a space-separated list of BCP47 language tags
      responses:
        200:
          description: OK
      tags:
      - Authorize
  /client:
    get:
      summary: List clients
      description: Retrieve a list of clients.
      operationId: client
      x-api-path-slug: client-get
      responses:
        200:
          description: OK
      tags:
      - Client
    post:
      summary: Register a client
      description: |-
        Register a new client with this Authentiq Connect provider.

        This endpoint is compatible with [OIDC's Client Registration](http://openid.net/specs/openid-connect-registration-1_0.html) extension.

        See also:
        - [OIDC Client Registration Endpoint](http://openid.net/specs/openid-connect-registration-1_0.html#ClientRegistration)
      operationId: createClient
      x-api-path-slug: client-post
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Client
  /client/{client_id}:
    delete:
      summary: Delete a client
      description: Delete a previously registered client.
      operationId: clientClient_id
      x-api-path-slug: clientclient-id-delete
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Client
      - Client
      - Id
    get:
      summary: View a client
      description: |-
        Retrieve the configuration of a previously registered client.

        See also:
        - [OIDC Client Configuration Endpoint](http://openid.net/specs/openid-connect-registration-1_0.html#ClientConfigurationEndpoint)
      operationId: getClient
      x-api-path-slug: clientclient-id-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Client
      - Client
      - Id
    put:
      summary: Update a client
      description: |-
        Update the configuration of a previously registered client.

        See also:
        - [OIDC Client Configuration Endpoint](http://openid.net/specs/openid-connect-registration-1_0.html#ClientConfigurationEndpoint)
      operationId: updateClient
      x-api-path-slug: clientclient-id-put
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Client
      - Client
      - Id
  /token:
    post:
      summary: Obtain an ID Token
      description: |-
        Exchange en authorization code for an ID Token or Access Token.

        This endpoint supports both `client_secret_post` and `client_secret_basic` authenticatino methods, as specified by the client's `token_endpoint_auth_method`.

        See also:
          - [OIDC Token Endpoint](http://openid.net/specs/openid-connect-core-1_0.html#TokenRequest)
          - [OIDC Successful Token response](http://openid.net/specs/openid-connect-core-1_0.html#TokenResponse)
          - [OIDC Token Error response](http://openid.net/specs/openid-connect-core-1_0.html#TokenError)
      operationId: token
      x-api-path-slug: token-post
      parameters:
      - in: header
        name: Authorization
        description: HTTP Basic authorization header
      - in: formData
        name: client_id
        description: The registered client ID
      - in: formData
        name: client_secret
        description: The registered client ID secret
      - in: formData
        name: code
        description: The authorization code previously obtained from the Authentication
          endpoint
      - in: formData
        name: grant_type
        description: The authorization grant type, must be `authorization_code`
      - in: formData
        name: redirect_uri
        description: The redirect URL that was used previously with the Authentication
          endpoint
      responses:
        200:
          description: OK
      tags:
      - Token
  /userinfo:
    get:
      summary: Retrieve their user profile
      description: |-
        Use this endpoint to retrieve a user's profile in case you've not already obtained enough details from the ID Token via the Token Endpoint.
         See also:
         - [OIDC UserInfo endpoint](http://openid.net/specs/openid-connect-core-1_0.html#UserInfo)
      operationId: userInfo
      x-api-path-slug: userinfo-get
      responses:
        200:
          description: OK
      tags:
      - Userinfo
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