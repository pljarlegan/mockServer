# mockServer

doc available here :
https://www.mock-server.com/mock_server/creating_expectations.html

# create new expectation

```shell
printf '{
    "httpRequest": {
        "path": "/some/path"
    },
    "httpResponse": {
      "headers": {
        "Content-Type": ["application/json"]
      },
      "body": {
        "type": "JSON",
        "json": {
          "some": "stuff"
        }
      }
    }
}'| http  --follow --timeout 3600 PUT 127.0.0.1/mock/expectation \
 Content-Type:'application/json'
```
