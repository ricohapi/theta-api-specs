# _ethernetConfig

### Overview

IP address allocation to be used when wired LAN is enabled.  

The current setting can be acquired by [camera.getOptions](../commands/camera.get_options.md), and it can be changed by [camera.setOptions](../commands/camera.set_options.md).

### Support model

| X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|
| v2.40.0 | --- | --- | --- | --- |

### Support value

| Value | Description |
|:--|:--|
| _ethernetConfig object |  |

### _ethernetConfig object
| Name | Type | Description |
|:--|:--|:--|
| ipAddressAllocation | String | `dynamic` or `static` <br> `dynamic` is default value. |
| ipAddress  | String | (optional) IPv4 for IP address  |
| subnetMask | String | (optional) IPv4 for subnet mask |
| defaultGateway | String | (optional) IPv4 for default gateway |
| _proxy | object | (optional) refer to [_proxy](./_proxy.md#_proxy-object) for detail |
