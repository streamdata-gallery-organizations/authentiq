{
  "info": {
    "name": "Authentiq Connect Delete a client",
    "_postman_id": "bf569a80-6b71-4fc8-8aa5-b8843d977163",
    "description": "Delete a previously registered client.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Authorize",
      "item": [
        {
          "id": "5019b429-8fa0-43ef-ae97-29c7ec949959",
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
              "id": "80a97572-82b1-4aa4-a81f-0bc539faa207"
            }
          ]
        }
      ]
    },
    {
      "name": "Client",
      "item": [
        {
          "id": "cf3967a0-526f-441b-aa1d-6466c7befeb0",
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
              "id": "0ffb376a-ec8d-4794-9ffe-8294cefb0f2f"
            }
          ]
        },
        {
          "id": "761483ba-de1e-41ba-82a2-c856dc88034e",
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
              "id": "451a5f90-c72d-4b9f-9349-8b8f9492800e"
            }
          ]
        },
        {
          "id": "bc40c0aa-aaf8-4020-8892-f3bc4fbc5a16",
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
              "id": "40fe9d72-4c40-4e40-bd27-5f907000c413"
            }
          ]
        }
      ]
    }
  ]
}