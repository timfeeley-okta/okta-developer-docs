### Web applications

Web applications introspect tokens by calling the `/introspect` endpoint and passing
in a required `Authorization` header. This header is computed from the client ID and
client secret.

Example

```http
POST /oauth2/default/v1/introspect HTTP/1.1
Accept: application/json
Content-Type: application/x-www-form-urlencoded
Authorization: Basic MG9hMTJncG5qZnpvdllTbk41ZDc6UG9zWGpjNmw0WHF5ZDBhek03cjF0SnhyMS1LWHdWYmNFaDk0Q0FDNA==

token=eyJraWQiOiJoQk...
token_type_hint=access_token
```
