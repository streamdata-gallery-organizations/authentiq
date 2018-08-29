{
  "info": {
    "name": "Authentiq Connect Retrieve their user profile",
    "_postman_id": "160746ea-83c3-4c33-a8f6-5ce878821016",
    "description": "Use this endpoint to retrieve a user's profile in case you've not already obtained enough details from the ID Token via the Token Endpoint.\n See also:\n - [OIDC UserInfo endpoint](http://openid.net/specs/openid-connect-core-1_0.html#UserInfo)",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Authorize",
      "item": [
        {
          "id": "53bd7710-2de1-4150-9bed-1e430dd01489",
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
              "id": "6976ec34-5a51-48ba-961b-7054eb765c58"
            }
          ]
        }
      ]
    },
    {
      "name": "Client",
      "item": [
        {
          "id": "20bafef9-a4d5-4a3e-9df2-d06f7e328c11",
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
              "id": "33c9c326-5255-424c-be68-f0944c7e5726"
            }
          ]
        },
        {
          "id": "986b0959-af16-4731-9ecd-5643a5e3d0fa",
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
              "id": "26d1df5e-93e7-4ac7-b071-1f7630c6f34d"
            }
          ]
        },
        {
          "id": "32d61047-5c25-40ea-ada3-aa1ff6deb954",
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
              "id": "033c3c4d-7e8d-44c1-86b1-ab4ad124fc49"
            }
          ]
        },
        {
          "id": "14c09d08-9fb4-45e8-9a83-6758fea2ab45",
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
              "id": "b23b57ba-c211-4aa3-80b1-542b05be282f"
            }
          ]
        },
        {
          "id": "aa0b484e-c463-406f-affe-86eff16959bb",
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
              "id": "91087bb2-cd55-4887-9bd7-e2f5bf7ee428"
            }
          ]
        }
      ]
    },
    {
      "name": "Token",
      "item": [
        {
          "id": "93bb2db2-6f81-4a16-a2a3-f8e29ead79e4",
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
              "id": "56f7cab2-55b4-4f6c-8713-3819fe33ad96"
            }
          ]
        }
      ]
    },
    {
      "name": "Userinfo",
      "item": [
        {
          "id": "7782fa9f-bf73-44ae-9cd8-9599ee7edd09",
          "name": "userInfo",
          "request": {
            "url": "http://connect.authentiq.io/userinfo",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Use this endpoint to retrieve a user's profile in case you've not already obtained enough details from the ID Token via the Token Endpoint.\n See also:\n - [OIDC UserInfo endpoint](http://openid.net/specs/openid-connect-core-1_0.html#UserInfo)"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f9185125-7bbc-4669-879b-b9e05e3fd950"
            }
          ]
        }
      ]
    }
  ]
}