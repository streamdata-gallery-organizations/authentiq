{
  "info": {
    "name": "Authentiq Connect Obtain an ID Token",
    "_postman_id": "17465c70-9d17-41b5-9f37-5b3d31396059",
    "description": "Exchange en authorization code for an ID Token or Access Token.\n\nThis endpoint supports both `client_secret_post` and `client_secret_basic` authenticatino methods, as specified by the client's `token_endpoint_auth_method`.\n\nSee also:\n  - [OIDC Token Endpoint](http://openid.net/specs/openid-connect-core-1_0.html#TokenRequest)\n  - [OIDC Successful Token response](http://openid.net/specs/openid-connect-core-1_0.html#TokenResponse)\n  - [OIDC Token Error response](http://openid.net/specs/openid-connect-core-1_0.html#TokenError)",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Authorize",
      "item": [
        {
          "id": "c624e937-b1c2-45c9-93af-b04b003cefa2",
          "name": "authorize",
          "request": {
            "url": "http://connect.authentiq.io/authorize?client_id=%7B%7D&display=%7B%7D&max_age=%7B%7D&nonce=%7B%7D&prompt=%7B%7D&redirect_uri=%7B%7D&response_mode=%7B%7D&response_type=%7B%7D&scope=%7B%7D&state=%7B%7D&ui_locales=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Start a session with Authentiq Connect and authenticate a user.\n\nExample:\n\n```\nGET https://connect.authentiq.io/authorize?client_id=<your-client-id>&response_type=code+id_token&scope=openid+email&redirect_uri=<your-redirect-uri>&state=0123456789\n```\n\nThis endpoint is compatible with OpenID Connect and also supports the POST method, in which case the parameters are passed as a form post.\n\nSee also:\n  - [OAuth 2.0 Authorization Endpoint](http://tools.ietf.org/html/rfc6749#section-3.1)\n  - [OIDC Authentication request](http://openid.net/specs/openid-connect-core-1_0.html#AuthRequest)\n  - [OIDC Successful Authentication response](http://openid.net/specs/openid-connect-core-1_0.html#AuthResponse)\n  - [OIDC Error Authentication response](http://openid.net/specs/openid-connect-core-1_0.html#AuthError)"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "81bd8953-a87e-4aee-8b62-13c50cbc1fea"
            }
          ]
        }
      ]
    },
    {
      "name": "Client",
      "item": [
        {
          "id": "8e1b2aec-6031-4fa0-8236-5c3a2fa727f6",
          "name": "client",
          "request": {
            "url": "http://connect.authentiq.io/client",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Retrieve a list of clients."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "dbc53939-03b6-4275-ac6a-a1a0239ea283"
            }
          ]
        },
        {
          "id": "a41e589c-af46-446f-98aa-bc5190e4f52f",
          "name": "createClient",
          "request": {
            "url": "http://connect.authentiq.io/client?No Name=%7B%7D",
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "Register a new client with this Authentiq Connect provider.\n\nThis endpoint is compatible with [OIDC's Client Registration](http://openid.net/specs/openid-connect-registration-1_0.html) extension.\n\nSee also:\n- [OIDC Client Registration Endpoint](http://openid.net/specs/openid-connect-registration-1_0.html#ClientRegistration)"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "0727bbc3-3324-4351-a317-2b4af1264d1f"
            }
          ]
        },
        {
          "id": "1e40786e-85a8-4959-925b-c30e4b3d06cc",
          "name": "getClient",
          "request": {
            "url": {
              "protocol": "http",
              "host": "connect.authentiq.io",
              "path": [
                "client/:client_id"
              ],
              "query": [
                {
                  "key": "No Name",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "client_id",
                  "value": "client_id",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Retrieve the configuration of a previously registered client.\n\nSee also:\n- [OIDC Client Configuration Endpoint](http://openid.net/specs/openid-connect-registration-1_0.html#ClientConfigurationEndpoint)"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f40c91a7-8b5c-4d6e-9c72-d6fe4376d281"
            }
          ]
        },
        {
          "id": "b836242a-8321-4b0a-9c8c-094839920bc3",
          "name": "updateClient",
          "request": {
            "url": {
              "protocol": "http",
              "host": "connect.authentiq.io",
              "path": [
                "client/:client_id"
              ],
              "query": [
                {
                  "key": "No Name",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "client_id",
                  "value": "client_id",
                  "type": "string"
                }
              ]
            },
            "method": "PUT",
            "body": {
              "mode": "raw"
            },
            "description": "Update the configuration of a previously registered client.\n\nSee also:\n- [OIDC Client Configuration Endpoint](http://openid.net/specs/openid-connect-registration-1_0.html#ClientConfigurationEndpoint)"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "1dfd625c-2a38-4efc-86a9-2234661b5f50"
            }
          ]
        },
        {
          "id": "5e4695ff-783e-4295-bb63-5d8f53c4d319",
          "name": "clientClient_id",
          "request": {
            "url": {
              "protocol": "http",
              "host": "connect.authentiq.io",
              "path": [
                "client/:client_id"
              ],
              "query": [
                {
                  "key": "No Name",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "client_id",
                  "value": "client_id",
                  "type": "string"
                }
              ]
            },
            "method": "DELETE",
            "body": {
              "mode": "raw"
            },
            "description": "Delete a previously registered client."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ea15efb3-c2de-465e-b5f0-916a6a30d492"
            }
          ]
        }
      ]
    },
    {
      "name": "Token",
      "item": [
        {
          "id": "c90b9751-8dc2-4bf9-8f61-00853de811b4",
          "name": "token",
          "request": {
            "url": "http://connect.authentiq.io/token",
            "method": "POST",
            "header": [
              {
                "key": "Authorization",
                "value": "{}",
                "description": "HTTP Basic authorization header",
                "disabled": false
              }
            ],
            "body": {
              "mode": "urlencoded",
              "urlencoded": [
                {
                  "key": "client_id",
                  "value": "{}",
                  "disabled": false,
                  "description": "The registered client ID"
                },
                {
                  "key": "client_secret",
                  "value": "{}",
                  "disabled": false,
                  "description": "The registered client ID secret"
                },
                {
                  "key": "code",
                  "value": "{}",
                  "disabled": false,
                  "description": "The authorization code previously obtained from the Authentication endpoint"
                },
                {
                  "key": "grant_type",
                  "value": "{}",
                  "disabled": false,
                  "description": "The authorization grant type, must be `authorization_code`"
                },
                {
                  "key": "redirect_uri",
                  "value": "{}",
                  "disabled": false,
                  "description": "The redirect URL that was used previously with the Authentication endpoint"
                }
              ]
            },
            "description": "Exchange en authorization code for an ID Token or Access Token.\n\nThis endpoint supports both `client_secret_post` and `client_secret_basic` authenticatino methods, as specified by the client's `token_endpoint_auth_method`.\n\nSee also:\n  - [OIDC Token Endpoint](http://openid.net/specs/openid-connect-core-1_0.html#TokenRequest)\n  - [OIDC Successful Token response](http://openid.net/specs/openid-connect-core-1_0.html#TokenResponse)\n  - [OIDC Token Error response](http://openid.net/specs/openid-connect-core-1_0.html#TokenError)"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "62507c5b-f4ce-46c2-aac0-52817bc690c4"
            }
          ]
        }
      ]
    }
  ]
}