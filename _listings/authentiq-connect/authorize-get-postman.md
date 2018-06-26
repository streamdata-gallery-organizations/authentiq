{
  "info": {
    "name": "Authentiq Connect Authenticate a user",
    "_postman_id": "397e7b9d-6983-42eb-a40f-fbc4500f1b33",
    "description": "Start a session with Authentiq Connect and authenticate a user.\n\nExample:\n\n```\nGET https://connect.authentiq.io/authorize?client_id=<your-client-id>&response_type=code+id_token&scope=openid+email&redirect_uri=<your-redirect-uri>&state=0123456789\n```\n\nThis endpoint is compatible with OpenID Connect and also supports the POST method, in which case the parameters are passed as a form post.\n\nSee also:\n  - [OAuth 2.0 Authorization Endpoint](http://tools.ietf.org/html/rfc6749#section-3.1)\n  - [OIDC Authentication request](http://openid.net/specs/openid-connect-core-1_0.html#AuthRequest)\n  - [OIDC Successful Authentication response](http://openid.net/specs/openid-connect-core-1_0.html#AuthResponse)\n  - [OIDC Error Authentication response](http://openid.net/specs/openid-connect-core-1_0.html#AuthError)",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Authorize",
      "item": [
        {
          "id": "fc924c4a-90b9-46a9-8d93-bb5e69357861",
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
              "id": "7911bf06-5992-42c4-94bc-21c5f4b9b8fa"
            }
          ]
        }
      ]
    }
  ]
}