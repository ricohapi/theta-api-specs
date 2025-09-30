# 0x99C0 SetAccessPointProxy

**Vendor Extension Operation**  
Sets the proxy information for the access point in client mode.  

### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) | ![SC](https://img.shields.io/badge/SC-orange) | ![S](https://img.shields.io/badge/S-red) |
|:-:|:-:|:-:|:-:|:-:|
|   | ✓<sup>\*1</sup> |   |   |   |

<sup>\*1</sup>Firmware v2.20.3 and later

| | |
|:--|:--|
| Operation Code | `0x99C0` |
| Operation Parameter 1 | `AccessPointHandle` |
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
| 2 | Url | 64 | STRING | Proxy server URL |
| 3 | Port | 5 | STRING | Proxy server port number: `0` to `65535` |
| 4 | UserID | 64 | STRING | User ID used for proxy authentication |
