# _accessInfo

### Overview

Return information related to connected access point and/or client device around wireless LAN and/or 4G/LTE.  
`_accessInfo` can be only GET by [camera.getOptions](../commands/camera.get_options.md).

### Support model

| X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|
| v2.10.1 | --- | --- | --- | --- |

### accessInfo Object

| Name | Type | Description |
|:--|:--:|:--|
|`ssid`          |String |SSID of the wireless LAN access point that THETA connects to|
|`ipAddress`     |String |IP address of access point \*1|
|`subnetMask`    |String |subnet mask of access point \*1|
|`defaultGateway`|String |default gateway of access point \*1|
|`proxyURL`      |String |proxy URL of access point \*1|
|`frequency`     |String |Radio frequency, e.g. `2.4` `5.2`|
|`wlanSignalStrength`|Int |[dBm]|
|`wlanSignalLevel`   |Int |`0`~`4`|
|`lteSignalStrength` |Int |[dBm]|
|`lteSignalLevel`    |Int |`0`~`4`|
|[`_dhcpLeaseAddress`](#_dhcpleaseaddress-object)\*2 |Object Array |client devices information|

\*1 : IPv4 address format  
\*2 : RICOH THETA X firmware v2.61.0 or later  

### _dhcpLeaseAddress Object

| Name | Type | Description |
|:--|:--:|:--|
|`ipAddress`     |String |IP address of client device \*1|
|`macAddress`    |String |MAC address of client device \*1|
|`hostName`      |String |host name of client device \*2|

\*1 : IPv4 address format  
\*2 : Some client device does not return its name.

#### Response Sample

```
"_dhcpLeaseAddress":[ 
{
    "ipAddress":"192.168.1.5", 
    "macAddress":"58:38:79:12:34:56", 
　　"hostName":"Macbook-Pro"
}, 
```
