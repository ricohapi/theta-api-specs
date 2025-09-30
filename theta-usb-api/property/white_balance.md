# 0x5005 WhiteBalance

Returns and sets the current setting of white balance mode.  
This setting is available in video recording mode on RICOH THETA V firmware v3.00.1 and later. Shooting settings are maintained separately for still capture mode and video recording mode.  

### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) | ![SC](https://img.shields.io/badge/SC-orange) | ![S](https://img.shields.io/badge/S-red) |
|:-:|:-:|:-:|:-:|:-:|
| ✓ | ✓ | ✓ | ✓ | ✓ |

| Field Order | Field Name | Size | Data Type | Description |
|:-:|:--|:-:|:--|:--|
| 1 | Property Code | 2 | UINT16 | `0x5005` |
| 2 | Datatype | 2 | UINT16 | `0x0004` (UINT16) |
| 3 | Get/Set | 1 | UINT8 | `0x01` (GET/SET) |
| 4 | Default Value | 2 | UINT16 | `0x0002` |
| 5 | Current Value | 2 | UINT16 ||
| 6 | Form Flag | 1 | UINT8 | `0x02` (Enumeration) |

### Supported Values

| Value | Description |
|:--|:--|
| `0x0002` | Automatic |
| `0x0004` | Outdoor |
| `0x8001` | Shade |
| `0x8002` | Cloudy |
| `0x0006` | Incandescent light 1 |
| `0x8020` | Incandescent light 2 |
| `0x8003` | Fluorescent light 1 (Daylight) |
| `0x8004` | Fluorescent light 2 (Natural white) |
| `0x8005` | Fluorescent light 3 (White) |
| `0x8006` | Fluorescent light 4 (Light bulb color) |
| `0x8007` | CT settings (specified by [`0xD813 ColorTemperature`](./color_temperature.md))<sup>\*1</sup> |
| `0x8008` | Underwater<sup>\*2\*3</sup> |

<sup>\*1</sup>THETA S firmware v1.82 and later, and RICOH THETA SC firmware v1.10 and later  
<sup>\*2</sup>THETA V firmware v3.21.1 and later  
<sup>\*3</sup>For THETA X, stitching process will be optimized for underwater setting when `0x5005 WhiteBalance` is set to `0x8008` Underwater.  
