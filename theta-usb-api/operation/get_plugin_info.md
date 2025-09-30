# 0x99A9 GetPluginInfo

**Vendor Extension Operation**  
Returns the detailed plugin information.  

### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) | ![SC](https://img.shields.io/badge/SC-orange) | ![S](https://img.shields.io/badge/S-red) |
|:-:|:-:|:-:|:-:|:-:|
| ✓ | ✓ | ✓<sup>\*1</sup> |   |   |

<sup>\*1</sup>Firmware v2.21.1 and later  

| | |
|:--|:--|
| Operation Code | `0x99A9` |
| Operation Parameter 1 | `PluginHandle` |
| Operation Parameter 2 | None |
| Operation Parameter 3 | None |
| Operation Parameter 4 | None |
| Operation Parameter 5 | None |
| Data | `PluginInfo` dataset |
| Data Direction | R->I |

### PluginInfo Dataset

| Field Order | Field Name | Size | Data Type | Description |
|:-:|:--|:-:|:--|:--|
| 1 | Plugin Name | Variable | String | Plugin name |
| 2 | Package Name | Variable | String | Plugin version |
| 3 | Version | Variable | String | Plugin version |
| 4 | Type | 1 | UINT8 | Type of application<br>`0`: Pre-installed plugin<br>`1`: User-added plugin |
| 5 | Running | 1 | UINT8 |  Plugin power status<br>`0`: Running, `1`: Stopped |
| 6 | Foreground | 1 | UINT8 | Plugin state<br>`0`: Foreground, `1`: Background |
| 7 | Boot<sup>\*2</sup> | 1 | UINT8 | Boot selection<br>`0`: Start this plugin (target plugin)<br>`1`: Do not start this plugin |
| 8 | Force | 1 | UINT8 | Plugin auto-start on boot<br>`0`: Disabled<br>`1`: Enabled |
| 9 | (Reserved) | Variable | String | Reserved |
| 10 | WebServer | 1 | UINT8 | Web server flag<br>`0`: Plugin provides a web server<br>`1`: Plugin does not provide a web server |
| 11 | Exit Status | 1 | UINT8 | Plugin termination status<br>`0`: Success<br>`1`: Error |
| 12 | Message | Variable | String | Message |

<sup>\*2</sup>THETA X supports only `0`.  
