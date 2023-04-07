# camera.\_setAccessPoint

### Overview

Sets the access point information used in client mode.  
Up to five access points can be registered. The access points registered with this API has priority over the ones detected with the camera UI.  

### Support model

| X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|
| v1.10.1 or later | All | v2.00.2 or later | --- | --- |

### Parameters

| Name | Type | Description |
|:--|:--|:--|
| ssid | String | SSID (Up to 32 bytes) |
| ssidStealth | Boolean | (Optional)<br>SSID stealth<br>(true: enable, false: disable. Default is false.) |
| security | String | (Mandatory)<br>Authentication mode<br>("none", "WEP", "WPA/WPA2 PSK")<br>This can be optional parameter only when overwriting access point information. \*1 |
| password | String | (Optional)<br>Password<br>This can be set when security is not "none" |
| connectionPriority | Number | (Optional)<br>(RICOH THETA V, Z1)<br>Connection priority (1 to 5). Default is 1.<br><br>(RICOH THETA X)<br>Fixed to 1 (The access point registered later has a higher priority.) |
| ipAddressAllocation | String | (Optional)<br>IP address allocation<br>"dynamic" or "static". Default is "dynamic" |
| ipAddress | String | (Optional)<br>IP address assigned to camera<br>This setting can be set when ipAddressAllocation is "static" |
| subnetMask | String | (Optional)<br>Subnet mask<br>This setting can be set when ipAddressAllocation is "static" |
| defaultGateway | String | (Optional)<br>Default gateway<br>This setting can be set when ipAddressAllocation is "static" |
| _proxy | Object | Proxy information to be used for the access point. |

\*1 Excluding THETA X.

### Results

None.
