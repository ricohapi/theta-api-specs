# 0x99AD SetAccessPointPassword

**Vendor Extension Operation**  
Sets the password for the access point in client mode.  

### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) | ![SC](https://img.shields.io/badge/SC-orange) | ![S](https://img.shields.io/badge/S-red) |
|:-:|:-:|:-:|:-:|:-:|
|   | ✓ | ✓<sup>\*1</sup> |   |   |

<sup>\*1</sup>Firmware v2.00.2 and later  

| | |
|:--|:--|
| Operation Code | `0x99AD` |
| Operation Parameter 1 | `AccessPointHandle` |
| Operation Parameter 2 | None |
| Operation Parameter 3 | None |
| Operation Parameter 4 | None |
| Operation Parameter 5 | None |
| Data | Password |
| Data Direction | I->R |

### Data

| Field Order | Field Name | Size | Data Type | Description |
|:-:|:--|:-:|:--|:--|
| 1 | Password | Variable | String | Password |
