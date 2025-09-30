# 0x99B8 GetPluginOrders

**Vendor Extension Operation**  
Returns the order of plugins displayed on the selection screen.  

### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) | ![SC](https://img.shields.io/badge/SC-orange) | ![S](https://img.shields.io/badge/S-red) |
|:-:|:-:|:-:|:-:|:-:|
| ✓ | ✓ |   |   |   |

#### THETA X

| | |
|:--|:--|
| Operation Code | `0x99B8` |
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
| 1 | `PluginHandle` array | Variable | AUINT32 | List of plugin handles |

A `PluginHandle` with an unregistered number returns `0xFFFFFFFF`.  

#### THETA Z1

| | |
|:--|:--|
| Operation Code | `0x99B8` |
| Operation Parameter 1 | None |
| Operation Parameter 2 | None |
| Operation Parameter 3 | None |
| Operation Parameter 4 | None |
| Operation Parameter 5 | None |
| Data | None |
| Data Direction | N/A |
| Response Parameter 1 | `PluginHandle` for Plugin 1 |
| Response Parameter 2 | `PluginHandle` for Plugin 2 |
| Response Parameter 3 | `PluginHandle` for Plugin 3 |
| Response Parameter 4 | None |
| Response Parameter 5 | None |
