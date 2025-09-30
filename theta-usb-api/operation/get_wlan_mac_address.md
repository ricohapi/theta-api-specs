# 0x99B5 GetWlanMacAddress

**Vendor Extension Operation**  
Returns the MAC address of the wireless LAN interface.  

### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) | ![SC](https://img.shields.io/badge/SC-orange) | ![S](https://img.shields.io/badge/S-red) |
|:-:|:-:|:-:|:-:|:-:|
| ✓ | ✓ | ✓<sup>\*1</sup> |   |   |

<sup>\*1</sup>Firmware v2.11.1 and later  

| | |
|:--|:--|
| Operation Code | `0x99B5` |
| Operation Parameter 1 | None |
| Operation Parameter 2 | None |
| Operation Parameter 3 | None |
| Operation Parameter 4 | None |
| Operation Parameter 5 | None |
| Data | `MacAddress` dataset |
| Data Direction | R->I |

### MacAddress Dataset

| Field Order | Field Name | Size | Data Type | Description |
|:-:|:--|:-:|:--|:--|
| 1 | MAC Address | 18 | String | MAC address |
