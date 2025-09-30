# 0x1001 GetDeviceInfo

Returns the device information.  
When the [`0x5002 FunctionalMode`](../property/functional_mode.md) property changes, any corresponding updates to the device information are notified via the [`0x4008 DeviceInfoChanged`](../event/device_info_changed.md) event.  

### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) | ![SC](https://img.shields.io/badge/SC-orange) | ![S](https://img.shields.io/badge/S-red) |
|:-:|:-:|:-:|:-:|:-:|
| ✓ | ✓ | ✓ | ✓ | ✓ |

| | |
|:--|:--|
| Operation Code | `0x1001` |
| Operation Parameter 1 | None |
| Operation Parameter 2 | None |
| Operation Parameter 3 | None |
| Operation Parameter 4 | None |
| Operation Parameter 5 | None |
| Data | `DeviceInfo` dataset |
| Data Direction | R->I |

### DeviceInfo Dataset 

| Field Order | Field Name | Size | Data Type | Description |
|:-:|:--|:-:|:--|:--|
| 1 | `Standard Version` | 2 | UINT16 ||
| 2 | `MTP Vendor Extension ID` | 4 | UINT32 | Fixed value |
| 3 | `MTP Version` | 2 | UINT16 | Fixed to `110` |
| 4 | `MTP Extension` | 4 | String ||
| 5 | `Functional Mode` | 2 | UINT16 | Camera status: refer to [`0x5002 FunctionalMode`](../property/functional_mode.md) property |
| 6 | `Operations Supported` | Variable || Operation Code Array |
| 7 | `Events Supported` | Variable || Event Code Array |
| 8 | `Device Properties Supported` | Variable || Device Property Code Array |
| 9 | `Capture Formats` | Variable || Object Format Code Array |
| 10 | `Playback Formats` | Variable || Object Format Code Array |
| 11 | `Manufacturer` | Variable | String ||
| 12 | `Model` | Variable | String ||
| 13 | `Device Version` | Variable | String | THETA firmware version |
| 14 | `Serial Number`  | Variable | String | THETA serial number |
