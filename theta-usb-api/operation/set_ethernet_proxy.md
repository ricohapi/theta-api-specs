# 0x99C3 SetEthernetProxy

**Vendor Extension Operation**  
Sets the proxy information for wired LAN.  

### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) | ![SC](https://img.shields.io/badge/SC-orange) | ![S](https://img.shields.io/badge/S-red) |
|:-:|:-:|:-:|:-:|:-:|
|   | ✓<sup>\*1</sup> |   |   |   |

<sup>\*1</sup>Firmware v2.20.3 and later

| | |
|:--|:--|
| Operation Code | `0x99C3` |
| Operation Parameter 1 | None |
| Operation Parameter 2 | None |
| Operation Parameter 3 | None |
| Operation Parameter 4 | None |
| Operation Parameter 5 | None |
| Data | `Proxy` dataset |
| Data Direction | I->R |

### Proxy Dataset

| Field Order | Field Name | Size | Data Type | Description |
|:-:|:--|:-:|:--|:--|
| 1 | Use | 1 | UINT8 | Proxy usage<br>`0`: Do not use proxy<br>`1`: Use proxy |
| 2 | Url | 64 | String | Proxy server URL |
| 3 | Port | 5 | String | Proxy server port number: `0` to `65535` |
| 4 | UserID | 64 | String | User ID used for proxy authentication |
