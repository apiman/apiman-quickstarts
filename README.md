apiman-quickstarts
==================

Some projects to help get started quickly with various aspects of apiman.

echo-service : Simple Echo Service replying to REST actions (get/post/put/delete). The service can be reached using a curl or Httpie request as presented hereafter

Example of request using HTTPie

```
http GET http://localhost:9999/apiman-echo/hello
``` 

Curl based example where json library has been installed using npm `npm install -g json` to format the request send or received

```
curl  -H "Accept: application/json" -H "Content-Type: application/json" -X GET http://localhost:9999/apiman-echo/hello | json

```

Remark : The servlet consuming the HTTP requests accepts any path (/*) and the put, post actions can include a HTTP Body.
