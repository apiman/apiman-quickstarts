Echo Service
============

This project produces a simple WAR that implements an "echo" REST web service, useful for testing
and demo'ing apiman.

Any request made to the echo service will respond with a 200 response code and a JSON response
body that includes all of the meta-data sent to the echo service in the request.  This means
that the request method, path, and headers are all wrapped into a JSON object and returned in
the body of the response.

For example, if the echo service is invoked like this:

----
http://localhost:8080/apiman-echo/sample/path
----

Then the response payload might be this:

----
{
  "method" : "GET",
  "resource" : "/apiman-echo/sample/path",
  "length" : -1,
  "uri" : "/apiman-echo/sample/path",
  "headers" : {
    "Accept-Language" : "en-US,en;q=0.5",
    "Host" : "localhost:8080",
    "Accept-Encoding" : "gzip, deflate",
    "User-Agent" : "Mozilla/5.0 (Windows NT 6.3; WOW64; rv:24.0) Gecko/20100101 Firefox/24.0",
    "Accept" : "text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8",
    "Connection" : "keep-alive"
  }
}
----

Deployment
==========

To deploy this demo to a running WildFly 8.x server, simply execute the following commands:

----
cd apiman-quickstarts/echo-service
mvn clean install
mvn wildfly:deploy
----
