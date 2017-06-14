{{{
  "title": "Using the API",
  "date": "03-25-2015",
  "author": "Bryan Friedman",
  "attachments": [],
  "related_products": [],
  "related_questions": [],
  "preview" : "Programmatically perform the same actions as the Control Portal.",
  "thumbnail": "../images/api-preview.png",
  "contentIsHTML": false
}}}

<iframe width="560" height="315" src="https://www.youtube.com/embed/2M4kMHHLm5Y" frameborder="0" allowfullscreen></iframe>

### Introduction

CenturyLink Public Cloud provides an API for performing the same actions programmatically as you can from within the Control Portal. This API is RESTful, using JSON messages over HTTP and relying on the standard HTTP verbs including `GET`, `POST`, `PUT`, `DELETE`, and `PATCH`. The general URL format of the service is: `https://api.ctl.io/v2/{resource}/{account alias}`.

The following demo uses raw HTTP requests to show an example of using the API to create a server. Of course, you may choose to use any programming language you like that supports handling HTTP requests and responses using JSON messages. For a full listing of all supported API methods, see our complete [API Documentation](//www.centurylinkcloud.com/api-docs/v2).

### Authenticate Against the API

Authentication to the API v2 is done with the same credentials used to access the CenturyLink Cloud Control Portal. The username and password are provided to the API and in return, the user gets back a credentials object. This object contains a valid bearer token which must be provided on each subsequent API request and can be reused for up to 2 weeks. The HTTP request must also include a `Content-Type` header set to `application/json`.

Below is an example of the raw HTTP request and response messages when retrieving a valid token from the API authentication service. (Note: The actual bearer token and password have been replaced with a random string for demonstration purposes.)

#### Request

    POST https://api.ctl.io/v2/authentication/login HTTP/1.1
    Host: api.ctl.io
    Content-Type: application/json

    {
      "username": "trent.anderson",
      "password": "P@ssw0rd1"
    }

#### Response

    HTTP/1.1 200 OK
    Cache-Control: no-cache
    Pragma: no-cache
    Content-Type: application/json; charset=utf-8
    Expires: -1
    Date: Thu, 26 Mar 2015 19:14:15 GMT
    Content-Length: 541

    {
      "roles" : [
        "ServerAdmin"
      ],
      "userName" : "trent.anderson",
      "bearerToken" : "VGCVlA1JK5WLEXicGVujiJblEIApnIJhicZcNZG1MjvJI5IQXJime3tzQYOYHjLuX2NiZLiJvTRi2JOXdcbkX46UWzmIZnJIzpM6JjpmJDB.iX91ML6IzhdX62cekloAB6uJUOjjoi1xClUOBXZmXJxciUzdje2MJM96VM1Mk4NOXubYIXbbiwf06E1YQbeEsKIy1HdizndJWyJVs4XCGiwpTdlyiRXkGrikopi0I5pI.6RYzOrI2lj4bYZsJzeWXGCRNpyXjIbbJLcJL3ckH4CjbisZnZJYMiiIYgD1plIa9JUXuFUG4iymCQV2JXiJluZiziRJYk0b1VJhIRc3M13ihOe",
      "accountAlias" : "BTDI",
      "locationAlias" : "WA1"
    }

These results show the user's parent account, default data center location, and assigned platform roles. The bearerToken is the value that must be added to the HTTP `Authorization` header when calling any other API service. This token identifies who the user is and what they are allowed to do in the API.

If you provide invalid credentials, you will get an HTTP 400 (Bad Request) and the following response message:

    HTTP/1.1 400 Bad Request
    Cache-Control: no-cache
    Pragma: no-cache
    Content-Type: application/json; charset=utf-8
    Expires: -1
    Date: Thu, 26 Mar 2015 19:15:22 GMT
    Content-Length: 89

    {"message":"We didn't recognize the username or password you entered. Please try again."}

### Call the Create Server API Endpoint

The following raw HTTP request message shows how a user can make a secure API request to create a server. Note that the `bearerToken` from the previous authentication call is added to the header of the request. The JSON payload also includes all the information required for a new server including the name, description, template, password, sizing info, and the identifier of the parent group to put the server in (obtained from the Control Portal URL for that group or a [link](http://www.centurylinkcloud.com/api-docs/v2/#getting-started-api-v20-links-framework) returned from a previous API call).

#### Request

    POST https://api.ctl.io/v2/servers/BTDI HTTP/1.1
    Host: api.ctl.io
    Content-Type: application/json
    Authorization: Bearer VGCVlA1JK5WLEXicGVujiJblEIApnIJhicZcNZG1MjvJI5IQXJime3tzQYOYHjLuX2NiZLiJvTRi2JOXdcbkX46UWzmIZnJIzpM6JjpmJDB.iX91ML6IzhdX62cekloAB6uJUOjjoi1xClUOBXZmXJxciUzdje2MJM96VM1Mk4NOXubYIXbbiwf06E1YQbeEsKIy1HdizndJWyJVs4XCGiwpTdlyiRXkGrikopi0I5pI.6RYzOrI2lj4bYZsJzeWXGCRNpyXjIbbJLcJL3ckH4CjbisZnZJYMiiIYgD1plIa9JUXuFUG4iymCQV2JXiJluZiziRJYk0b1VJhIRc3M13ihOe

    {
      "name": "rhel",
      "description": "My RedHat Server",
      "groupId": "60582771e45fe111ba2500505682315a",
      "sourceServerId": "RHEL-6-64-TEMPLATE",
      "password": "P@ssw0rd1",
      "cpu": 2,
      "memoryGB": 4,
      "type": "standard",
      "storageType": "standard"
    }

The response is `HTTP 202 Accepted` (instead of `HTTP 200 OK`) which indicates that the request is a long-running process and a job was added to the queue to complete the server build. A JSON message is also returned with information about the newly requested server and a link to the [job status API](http://www.centurylinkcloud.com/api-docs/v2/#queue-get-status) endpoint to further track the completion of the request.

#### Response

    HTTP/1.1 202 Accepted
    Cache-Control: no-cache
    Pragma: no-cache
    Content-Type: application/json; charset=utf-8
    Expires: -1
    Date: Thu, 26 Mar 2015 22:27:24 GMT
    Content-Length: 265

    {
      "server" : "rhel",
      "isQueued" : true,
      "links" : [
        {
          "rel" : "status",
          "id" : "wa1-143253",
          "href" : "/v2/operations/btdi/status/wa1-143253"
        },
        {
          "rel" : "self",
          "id" : "be96b91d4eef4789b81184992c9ac821",
          "href" : "/v2/servers/BTDI/be96b91d4eef4789b81184992c9ac821?uuid=True",
          "verbs" : [
            "GET"
          ]
        }
      ]
    }
