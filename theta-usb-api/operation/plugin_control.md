# 0x99AB PluginControl

**Vendor Extension Operation**  
Starts or stops the plugin.  

### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) | ![SC](https://img.shields.io/badge/SC-orange) | ![S](https://img.shields.io/badge/S-red) |
|:-:|:-:|:-:|:-:|:-:|
| ✓ | ✓ | ✓<sup>\*1</sup> |   |   |

<sup>\*1</sup>Firmware v2.21.1 and later  

| | |
|:--|:--|
| Operation Code | `0x99AB` |
| Operation Parameter 1 | `0`: Starts the plugin<br>`1`: Stops the plugin |
| Operation Parameter 2 | `PluginHandle`<sup>\*2</sup> |
| Operation Parameter 3 | None |
| Operation Parameter 4 | None |
| Operation Parameter 5 | None |
| Data | None |
| Data Direction | N/A |

<sup>\*2</sup>This parameter is ignored when the plugin is stopped.  
