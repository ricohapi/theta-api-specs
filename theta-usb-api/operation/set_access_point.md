# 0x99A5 SetAccessPoint

**Vendor Extesion Operation**  
Sets the access point information for use in client mode.  

#### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) | ![SC](https://img.shields.io/badge/SC-orange) | ![S](https://img.shields.io/badge/S-red) |
|:-:|:-:|:-:|:-:|:-:|
|   | ✓ | ✓<sup>\*1</sup> |   |   |

<sup>\*1</sup>Firmware v2.00.2 and later  

| | |
|:--|:--|
| Operation Code | `0x99A5` |
| Operation Parameter 1 | None |
| Operation Parameter 2 | None |
| Operation Parameter 3 | None |
| Operation Parameter 4 | None |
| Operation Parameter 5 | None |
| Data | `AccessPointInfo` dataset |
| Data Direction | I->R |

### AccessPointInfo Dataset

| Field Order | Field Name | Size | Data Type | Description |
|:-:|:--|:-:|:--|:--|
| 1 | SSID | Variable | String | SSID |
| 2 | SSID Stealth | 1 | UINT8 | `0`: Disabled<br>`1`: Eabled |
| 3 | Security | Variable | String | Authentication mode<br>`none`, `WEP`, `WPA/WPA2 PSK` |
| 4 | Connection Priority | 1 | UINT8 | `1` to `5` |
| 5 | IP Address Allocation | 1 | UINT8 | `0`: Dynamic<br>`1`: Static |
| 6 | IP Address | 4 | UINT32 | IP address assigned to camera<sup>\*2</sup> |
| 7 | Subnet Mask | 4 | UINT32 | Subnet mask<sup>\*2</sup> |
| 8 | Default Gateway | 4 | UINT32 | Default gateway<sup>\*2</sup> |

<sup>\*2</sup>This can be acquired when IP Address Allocation is `1`.  
