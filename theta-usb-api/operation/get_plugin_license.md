# 0x99B3 GetPluginLicense

**Vendor Extension Operation**  
Returns the license information for the installed plugin.  

#### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) | ![SC](https://img.shields.io/badge/SC-orange) | ![S](https://img.shields.io/badge/S-red) |
|:-:|:-:|:-:|:-:|:-:|
| ✓ | ✓ | ✓<sup>\*1</sup> |   |   |

<sup>\*1</sup>Firmware v2.21.1 and later  

| | |
|:--|:--|
| Operation Code | `0x99B3` |
| Operation Parameter 1 | `PluginHandle` |
| Operation Parameter 2 | None |
| Operation Parameter 3 | None |
| Operation Parameter 4 | None |
| Operation Parameter 5 | None |
| Data | License File |
| Data Direction | R->I |

### Data

| Field Order | Field Name | Size | Data Type | Description |
|:-:|:--|:-:|:--|:--|
| 1 | License File | Variable | String | Contents of the license files |
