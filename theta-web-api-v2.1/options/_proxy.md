# _proxy

### Overview

Proxy information to be used when wired LAN is enabled.

The current setting can be acquired by [camera.getOptions](../commands/camera.get_options.md), and it can be changed by [camera.setOptions](../commands/camera.set_options.md).

### Support model

| X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|
| v2.00.0 and later | v2.20.3 and later | --- | --- | --- |

### Support value

| Value | Description |
|:--|:--|
| _proxy object | Proxy information to be used when wired LAN is enabled. |

### _proxy object
| Name | Type | Description |
|:--|:--|:--|
| use | Boolean | true: use proxy false: do not use proxy |
| url | String | Proxy server URL |
| port | Number | Proxy server port number: 0 to 65535 |
| userid | String | User ID used for proxy authentication |
| password | String | Password used for proxy authentication |
