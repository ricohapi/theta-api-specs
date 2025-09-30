# 0x99B7 SetPluginOrders

**Vendor Extension Operation**  
Sets the order of plugins displayed on the selection screen.  

### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) | ![SC](https://img.shields.io/badge/SC-orange) | ![S](https://img.shields.io/badge/S-red) |
|:-:|:-:|:-:|:-:|:-:|
| ✓ | ✓ |   |   |   |

#### THETA X

| | |
|:--|:--|
| Operation Code | `0x99B7` |
| Operation Parameter 1 | None |
| Operation Parameter 2 | None |
| Operation Parameter 3 | None |
| Operation Parameter 4 | None |
| Operation Parameter 5 | None |
| Data | `PluginHandle` array |
| Data Direction | I->R |

### Data

| Field Order | Field Name | Size | Data Type | Description |
|:-:|:--|:-:|:--|:--|
| 1 | `PluginHandle` array | Variable | AUINT32 | List of plugin handles |

1. Registers plugins in the order specified by the `PluginHandle` array.
2. For unregistered entries, set the PluginHandle value to `0xFFFFFFFF`.
3. A plugin specified in the n-th element of the array is registered as entry n+1.
4. If a plugin not specified by this API is already registered on the camera, the plugins specified by this API are registered starting from the first entry.

#### THETA Z1

| | |
|:--|:--|
| Operation Code | `0x99B7` |
| Operation Parameter 1 | `PluginHandle` for Plugin 1 |
| Operation Parameter 2 | `PluginHandle` for Plugin 2 |
| Operation Parameter 3 | `PluginHandle` for Plugin 3 |
| Operation Parameter 4 | None |
| Operation Parameter 5 | None |
| Data | None |
| Data Direction | N/A |

If not specified, set the value to `0xFFFFFFFF`.  
If `0xFFFFFFFF` is placed in the middle of the array, it will be moved to the beginning.  
Specifying no plugin results in an error.
