# 0x99C4 SetEthernetProxyPassword

**Vendor Extension Operation**  
Sets the proxy password for for wired LAN.  

### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) | ![SC](https://img.shields.io/badge/SC-orange) | ![S](https://img.shields.io/badge/S-red) |
|:-:|:-:|:-:|:-:|:-:|
|   | ✓<sup>\*1</sup> |   |   |   |

<sup>\*1</sup>Firmware v2.20.3 and later  

| | |
|:--|:--|
| Operation Code | `0x99C4` |
| Operation Parameter 1 | None |
| Operation Parameter 2 | None |
| Operation Parameter 3 | None |
| Operation Parameter 4 | None |
| Operation Parameter 5 | None |
| Data | `ProxyPassword` dataset |
| Data Direction | I->R |

### ProxyPassword Dataset

| Field Order | Field Name | Size | Data Type | Description |
|:-:|:--|:-:|:--|:--|
| 1 | ProxyPassword | 64 | String | Proxy authentication password |
