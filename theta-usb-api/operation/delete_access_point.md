# 0x99A6 DeleteAccessPoint

**Vendor Extension Operation**

Deletes the access point information for use in client mode.  

#### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) | ![SC](https://img.shields.io/badge/SC-orange) | ![S](https://img.shields.io/badge/S-red) |
|:-:|:-:|:-:|:-:|:-:|
|   | ✓ | ✓<sup>\*1</sup> |   |   |

<sup>\*1</sup>Firmware v2.00.2 and later  

| | |
|:--|:--|
| Operation Code | `0x99A6` |
| Operation Parameter 1 | `AccessPointHandle` |
| Operation Parameter 2 | None<sup>\*2</sup> |
| Operation Parameter 3 | None<sup>\*2</sup> |
| Operation Parameter 4 | None<sup>\*2</sup> |
| Operation Parameter 5 | None<sup>\*2</sup> |
| Data | None |
| Data Direction | N/A |

<sup>\*2</sup>Unused. Specify `0x00000000`.  
