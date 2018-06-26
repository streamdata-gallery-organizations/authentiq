{
  "info": {
    "name": "Authentiq Connect View a client",
    "_postman_id": "6e3ae186-c51b-4188-b91c-72ded2637a4b",
    "description": "Retrieve the configuration of a previously registered client.\n\nSee also:\n- [OIDC Client Configuration Endpoint](http://openid.net/specs/openid-connect-registration-1_0.html#ClientConfigurationEndpoint)",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Authorize",
      "item": [
        {
          "id": "7a07e1a1-da6d-4542-b486-cb64daa791f7",
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
              "id": "2474a8a1-4b9c-4135-977d-2feb5183d37b"
            }
          ]
        }
      ]
    },
    {
      "name": "Client",
      "item": [
        {
          "id": "20eee89b-ed3f-441f-886f-338719f72b39",
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
              "id": "9611ce6b-4d68-413a-8ab2-2e789fb3af06"
            }
          ]
        },
        {
          "id": "6cf09f8a-5490-4012-8dca-5e0210d2e40d",
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
              "id": "c1986358-8b4e-4df8-bd06-02db076a011c"
            }
          ]
        },
        {
          "id": "5e464351-ca17-4e61-abfb-294136402739",
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
              "id": "55c7fe6f-9637-42f1-9117-06fac8a7a12f"
            }
          ]
        },
        {
          "id": "567486ee-7a50-4bfb-aadd-5e993c45708a",
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
              "id": "b80c7a89-425a-4799-a7cb-6540ede19e40"
            }
          ]
        }
      ]
    }
  ]
}