# camera.\_listAccessPoints

### Overview

Acquires the access point list used in client mode.  
For RICOH THETA X, only the access points registered with [camera._setAccessPoint](camera._set_access_point.md) can be acquired. (The access points automatically detected with the camera UI cannot be acquired with this API.)  

### Support model

| X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|
| v1.10.1 and later | All | v2.00.2 and later | --- | --- |

### Parameters

None.

### Results

| Name | Type | Description |
|:--|:--|:--|
| accessPoints | Object | Lists the access points stored on the camera and the access points detected by the camera.<br>See the next section for details. |

### accessPoints object

| Name | Type | Description |
|:--|:--|:--|
| ssid | String | SSID |
| ssidStealth | Boolean | True if SSID stealth is enabled |
| security | String | Authentication mode |
| connectionPriority | Number | Connection priority |
| ipAddressAllocation | String | IP address allocation<br>This can be acquired when SSID is registered as an enable access point. |
| ipAddress | String | IP address assigned to camera<br>This setting can be acquired when "ipAddressAllocation" is "static" |
| subnetMask | String | Subnet Mask<br>This setting can be acquired when "ipAddressAllocation" is "static" |
| defaultGateway | String | Default Gateway<br>This setting can be acquired when "ipAddressAllocation" is "static" |
| _proxy | Object | Proxy information to be used for the access point. *2 *3<br>Also refer to [_proxy](../options/_proxy.md) option spec to get each parameter.  |

*2 THETA Z1 Version 2.20.3 and later  
*3 THETA X Version 2.00.0 and later
