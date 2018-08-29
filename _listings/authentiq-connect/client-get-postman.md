{
  "info": {
    "name": "Authentiq Connect List clients",
    "_postman_id": "5d2fa8f7-4869-441b-bcc8-b00fcca5fa04",
    "description": "Retrieve a list of clients.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Authorize",
      "item": [
        {
          "id": "01236597-6458-4c9b-ac00-f630584eefb1",
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
              "id": "543fc07b-73af-44f4-a6bb-1aa3958054be"
            }
          ]
        }
      ]
    },
    {
      "name": "Client",
      "item": [
        {
          "id": "a98f2170-24aa-4633-91b5-307f1ed63f5c",
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
              "id": "acdf1873-b15d-4d2d-a42a-2442183d4017"
            }
          ]
        }
      ]
    }
  ]
}