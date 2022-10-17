# Overview

RICOH THETA API v2.0 is compliant with [Open Spherical Camera API Version 1.0](https://developers.google.com/streetview/open-spherical-camera/) (OSC) from Google. Furthermore, in addition to the API stipulated in the OSC, the API is extended to accommodate the RICOH THETA original functions. Command names and parameter names that are original extensions can be identified by the "\_ (underscore)" at the start of the name.

Wireless LAN is used for communication between the client and RICOH THETA. RICOH THETA operates as an HTTP server when the wireless LAN is ON, and API can be used for GET requests and POST requests.

Acquire the prerequisite specifications from the link below.

- [Open Spherical Camera API](https://developers.google.com/streetview/open-spherical-camera/)

### IP address and port

192.168.1.1:80

### Request/Response Example

#### Request

```
[API (e.g. POST /osc/commands/execute)] HTTP/1.1
Host: [IP address]:[HTTP port]
Content-Type: application/json;charset=utf-8
Accept: application/json
Content-Length: [Content length]

{
  ...
  each API Input
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
  each API Output
  ...
}
```
