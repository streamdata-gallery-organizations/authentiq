{
  "info": {
    "name": "Authentiq Connect Update a client",
    "_postman_id": "ec9908ee-a6f2-47ae-ba83-83a2bc30b8e7",
    "description": "Update the configuration of a previously registered client.\n\nSee also:\n- [OIDC Client Configuration Endpoint](http://openid.net/specs/openid-connect-registration-1_0.html#ClientConfigurationEndpoint)",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Authorize",
      "item": [
        {
          "id": "6f6ac3d9-ae5a-4c05-a488-7a04a75c1764",
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
              "id": "7c43c958-5e07-44c4-893a-ca86e2acdf1b"
            }
          ]
        }
      ]
    },
    {
      "name": "Client",
      "item": [
        {
          "id": "a68760aa-4124-4037-b644-18e911f5107c",
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
              "id": "931c4791-b824-4170-91a9-360c926f959a"
            }
          ]
        },
        {
          "id": "90c0189b-39b4-481b-b9e2-47c95a39e422",
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
              "id": "e1f4c525-488e-4fba-b059-e41228189346"
            }
          ]
        },
        {
          "id": "10752554-1a70-480d-90ba-1975ca707694",
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
              "id": "c142bbaf-cd03-461c-97c9-2f1985ff8fac"
            }
          ]
        },
        {
          "id": "9dd63f24-03f8-457d-a02b-3b206701c28c",
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
              "id": "f4eb5ab8-4870-42cd-b652-b138bb0ea4a0"
            }
          ]
        },
        {
          "id": "16ea6d94-57c2-46b2-9a63-9b22583793de",
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
              "id": "ff95f790-67c0-4c2d-990f-9b593623f6ab"
            }
          ]
        }
      ]
    }
  ]
}