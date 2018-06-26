---
name: Authentiq Connect
x-slug: authentiq-connect
description: Authentiq offers the convenience of passwordless authentication with
  the safety of two step verification. Sign up for Authentiq today, and never think
  about authentication again.
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/authentiq-logo.png
x-kinRank: "7"
x-alexaRank: "0"
tags: Authentiq Connect
created: "2018-06-26"
modified: "2018-06-26"
url: https://raw.githubusercontent.com/streamdata-gallery-organizations/authentiq-connect/master/_listings/authentiq-connect/apis.md
specificationVersion: "0.14"
apis:
- name: Authentiq Connect Authenticate a user
  x-api-slug: authentiq-connect
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
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/authentiq-logo.png
  humanURL: http://authentiq.com
  baseURL: https://connect.authentiq.io////authorize
  tags: Authorize
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/authentiq-connect/master/_listings/authentiq-connect/authorize-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/authentiq-connect/master/_listings/authentiq-connect/authorize-get-openapi.md
- name: Authentiq Connect List clients
  x-api-slug: authentiq-connect
  description: Retrieve a list of clients.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/authentiq-logo.png
  humanURL: http://authentiq.com
  baseURL: https://connect.authentiq.io////client
  tags: Client
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/authentiq-connect/master/_listings/authentiq-connect/client-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/authentiq-connect/master/_listings/authentiq-connect/client-get-openapi.md
- name: Authentiq Connect Register a client
  x-api-slug: authentiq-connect
  description: |-
    Register a new client with this Authentiq Connect provider.

    This endpoint is compatible with [OIDC's Client Registration](http://openid.net/specs/openid-connect-registration-1_0.html) extension.

    See also:
    - [OIDC Client Registration Endpoint](http://openid.net/specs/openid-connect-registration-1_0.html#ClientRegistration)
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/authentiq-logo.png
  humanURL: http://authentiq.com
  baseURL: https://connect.authentiq.io////client
  tags: Client
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/authentiq-connect/master/_listings/authentiq-connect/client-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/authentiq-connect/master/_listings/authentiq-connect/client-post-openapi.md
- name: Authentiq Connect Delete a client
  x-api-slug: authentiq-connect
  description: Delete a previously registered client.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/authentiq-logo.png
  humanURL: http://authentiq.com
  baseURL: https://connect.authentiq.io////client/{client_id}
  tags: Client,Client,Id
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/authentiq-connect/master/_listings/authentiq-connect/clientclient-id-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/authentiq-connect/master/_listings/authentiq-connect/clientclient-id-delete-openapi.md
- name: Authentiq Connect View a client
  x-api-slug: authentiq-connect
  description: |-
    Retrieve the configuration of a previously registered client.

    See also:
    - [OIDC Client Configuration Endpoint](http://openid.net/specs/openid-connect-registration-1_0.html#ClientConfigurationEndpoint)
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/authentiq-logo.png
  humanURL: http://authentiq.com
  baseURL: https://connect.authentiq.io////client/{client_id}
  tags: Client,Client,Id
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/authentiq-connect/master/_listings/authentiq-connect/clientclient-id-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/authentiq-connect/master/_listings/authentiq-connect/clientclient-id-get-openapi.md
- name: Authentiq Connect Update a client
  x-api-slug: authentiq-connect
  description: |-
    Update the configuration of a previously registered client.

    See also:
    - [OIDC Client Configuration Endpoint](http://openid.net/specs/openid-connect-registration-1_0.html#ClientConfigurationEndpoint)
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/authentiq-logo.png
  humanURL: http://authentiq.com
  baseURL: https://connect.authentiq.io////client/{client_id}
  tags: Client,Client,Id
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/authentiq-connect/master/_listings/authentiq-connect/clientclient-id-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/authentiq-connect/master/_listings/authentiq-connect/clientclient-id-put-openapi.md
- name: Authentiq Connect Obtain an ID Token
  x-api-slug: authentiq-connect
  description: |-
    Exchange en authorization code for an ID Token or Access Token.

    This endpoint supports both `client_secret_post` and `client_secret_basic` authenticatino methods, as specified by the client's `token_endpoint_auth_method`.

    See also:
      - [OIDC Token Endpoint](http://openid.net/specs/openid-connect-core-1_0.html#TokenRequest)
      - [OIDC Successful Token response](http://openid.net/specs/openid-connect-core-1_0.html#TokenResponse)
      - [OIDC Token Error response](http://openid.net/specs/openid-connect-core-1_0.html#TokenError)
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/authentiq-logo.png
  humanURL: http://authentiq.com
  baseURL: https://connect.authentiq.io////token
  tags: Token
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/authentiq-connect/master/_listings/authentiq-connect/token-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/authentiq-connect/master/_listings/authentiq-connect/token-post-openapi.md
- name: Authentiq Connect Retrieve their user profile
  x-api-slug: authentiq-connect
  description: |-
    Use this endpoint to retrieve a user's profile in case you've not already obtained enough details from the ID Token via the Token Endpoint.
     See also:
     - [OIDC UserInfo endpoint](http://openid.net/specs/openid-connect-core-1_0.html#UserInfo)
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/authentiq-logo.png
  humanURL: http://authentiq.com
  baseURL: https://connect.authentiq.io////userinfo
  tags: Userinfo
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/authentiq-connect/master/_listings/authentiq-connect/userinfo-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/authentiq-connect/master/_listings/authentiq-connect/userinfo-get-openapi.md
- name: Authentiq Connect Include a session iframe
  x-api-slug: authentiq-connect
  description: |-
    An OpenID Connect Session Management iframe to facilitate e.g. single sign-on or remote logouts.

    The iframe implements the OIDC postMessage-based [change notification protocol](http://openid.net/specs/openid-connect-session-1_0.html#ChangeNotification) via which a client can receive notifications about session state changes.

    See also:
    - [OIDC OP iframe](http://openid.net/specs/openid-connect-session-1_0.html#OPiframe)
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/authentiq-logo.png
  humanURL: http://authentiq.com
  baseURL: https://connect.authentiq.io////{client_id}/iframe
  tags: Client,Id,Iframe
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/authentiq-connect/master/_listings/authentiq-connect/client-idiframe-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/authentiq-connect/master/_listings/authentiq-connect/client-idiframe-get-openapi.md
- name: Authentiq Connect
  x-api-slug: authentiq-connect
  description: Authentiq offers the convenience of passwordless authentication with
    the safety of two step verification. Sign up for Authentiq today, and never think
    about authentication again.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/authentiq-logo.png
  humanURL: http://authentiq.com
  baseURL: https://connect.authentiq.io//
  tags: Authentiq Connect
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/authentiq-connect/master/_listings/authentiq-connect/openapi.md
x-common:
- type: x-website
  url: http://authentiq.com
- type: x-blog
  url: https://www.authentiq.com/blog/
- type: x-developer
  url: https://www.authentiq.com/developers/
- type: x-github
  url: https://github.com/AuthentiqID
- type: x-pricing
  url: https://www.authentiq.com/pricing/
- type: x-twitter
  url: AuthentiqID
- type: x-website
  url: http://authentiq.io
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---