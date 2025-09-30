# Overview

RICOH THETA API v2.1 (supported by RICOH THETA S firmware v01.62 and later) conforms to [Open Spherical Camera API Version 2.0](https://developers.google.com/streetview/open-spherical-camera/) (OSC) by Google. In addition to APIs defined by OSC, APIs extended for the proprietary to RICOH THETA are provided. Extended APIs can be identified by an "\_" (underscore) prepended to the name of a command or parameter.

Wireless LAN is used for communication between a client and RICOH THETA. While wireless LAN connection is ON, RICOH THETA acts as an HTTP server and can use APIs by GET and POST requests.

Obtain the base specifications from the following:

- [Open Spherical Camera API](https://developers.google.com/streetview/open-spherical-camera/)

### IP address and port

192.168.1.1:80 in direct mode.

In client mode, as in [camera.\_listAccessPoints](commands/camera._list_access_points.md) (RICOH THETA V firmware v2.00.2 and later).

### Request and response example

#### Request

```
[API (e.g. POST /osc/commands/execute)] HTTP/1.1
Host: [IP address]:[HTTP port]
Content-Type: application/json;charset=utf-8
Accept: application/json
Content-Length: [Content length]

{
  ...
  Input to each API
  ...
}
```

#### Response

```
HTTP/1.1 200 OK
Content-Type: application/json;charset=utf-8
Content-Length: [Content length]
X-Content-Type-Options: nosniff

{
  ...
  Output from each API
  ...
}
```

### Acquiring a file and thumbnail

API v2.1 allows for acquiring a binary resource by a GET request for the file URL.  
 To acquire a thumbnail, add a query "type=thumb" to the URL.  
 Refer to [Getting Started](getting_started.md) for an example of acquiring a binary resource.
