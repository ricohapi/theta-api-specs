# 0x99A3 GetAccessPointHandles

**Vendor Extension Operations**  
Returns the list of access point handles used in client mode.  

### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) | ![SC](https://img.shields.io/badge/SC-orange) | ![S](https://img.shields.io/badge/S-red) |
|:-:|:-:|:-:|:-:|:-:|
|   | ✓ | ✓<sup>\*1</sup> |   |   |

<sup>\*1</sup>Firmware v2.00.2 and later  

| | |
|:--|:--|
| Operation Code | `0x99A3` |
| Operation Parameter 1 | None |
| Operation Parameter 2 | None |
| Operation Parameter 3 | None |
| Operation Parameter 4 | None |
| Operation Parameter 5 | None |
| Data | `AccessPointHandle` array |
| Data Direction | R->I |


### Data

| Field Order | Field Name | Size | Data Type | Description |
|:-:|:--|:-:|:--|:--|
| 1 | `AccessPointHandle` array | Variable | AUINT32 | The list of access point handles |
