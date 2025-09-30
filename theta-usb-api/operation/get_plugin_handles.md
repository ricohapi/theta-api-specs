# 0x99A8 GetPluginHandles

**Vendor Extension Operation**  
Returns the list of plugin handles.  

#### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) | ![SC](https://img.shields.io/badge/SC-orange) | ![S](https://img.shields.io/badge/S-red) |
|:-:|:-:|:-:|:-:|:-:|
|   | ✓ | ✓<sup>\*1</sup> |   |   |

<sup>\*1</sup>Firmware v2.21.1 and later  

| | |
|:--|:--|
| Operation Code | `0x99A8` |
| Operation Parameter 1 | None |
| Operation Parameter 2 | None |
| Operation Parameter 3 | None |
| Operation Parameter 4 | None |
| Operation Parameter 5 | None |
| Data | `PluginHandle` array |
| Data Direction | R->I |

### Data

| Field Order | Field Name | Size | Data Type | Description |
|:-:|:--|:-:|:--|:--|
| 1 | `PluginHandle` array | Variable | AUINT32 | The list of plugin handles |
