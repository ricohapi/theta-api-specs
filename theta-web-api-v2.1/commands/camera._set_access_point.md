# camera.\_setAccessPoint

### Overview

Sets the access point information used in client mode.  
Up to five access points can be registered. The access points registered with this API has priority over the ones detected with the camera UI.  

### Support model

| X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|
| v1.10.1 and later | All | v2.00.2 and later | --- | --- |

### Parameters

| Name | Type | Description |
|:--|:--|:--|
| ssid | String | SSID (Up to 32 bytes) |
| ssidStealth | Boolean | (Optional)<br>SSID stealth<br>(true: enable, false: disable. Default is false.) |
| security | String | (Mandatory)<br>Authentication mode<br>("none", "WEP", "WPA/WPA2 PSK")<br>This can be optional parameter only when overwriting access point information. |
| password | String | (Optional)<br>Password<br>This can be set when security is not "none" |
| connectionPriority | Number | (Optional)<br>(RICOH THETA V, Z1)<br>Connection priority (1 to 5). Default is 1.<br><br>(RICOH THETA X)<br>Fixed to 1 (The access point registered later has a higher priority.) |
| ipAddressAllocation | String | (Optional)<br>IP address allocation<br>"dynamic" or "static". Default is "dynamic" |
| ipAddress | String | (Optional)<br>IP address assigned to camera<br>This setting must be set when ipAddressAllocation is "static" |
| subnetMask | String | (Optional)<br>Subnet mask<br>This setting must be set when ipAddressAllocation is "static" |
| defaultGateway | String | (Optional)<br>Default gateway<br>This setting must be set when ipAddressAllocation is "static" |
| _proxy | Object | Proxy information to be used for the access point. *2 *3<br>Also refer to [_proxy](../options/_proxy.md) option spec to set each parameter.  |

*2 THETA Z1 Version 2.20.3 and later  
*3 THETA X Version 2.00.0 and later

### Results

None.
