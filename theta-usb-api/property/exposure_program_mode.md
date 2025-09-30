# 0x500E ExposureProgramMode

Returns and sets the current setting of exposure program.  
This setting is available in video recording mode on RICOH THETA V firmware v3.00.1 and later. Shooting settings are maintained separately for still capture mode and video recording mode.  

### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) | ![SC](https://img.shields.io/badge/SC-orange) | ![S](https://img.shields.io/badge/S-red) |
|:-:|:-:|:-:|:-:|:-:|
| ✓ | ✓ | ✓ | ✓ | ✓ |

| Field Order | Field Name | Size | Data Type | Description |
|:-:|:--|:-:|:--|:--|
| 1 | Property Code | 2 | UINT16 | `0x500E` |
| 2 | Datatype | 2 | UINT16 | `0x0004` (UINT16) |
| 3 | Get/Set | 1 | UINT8 | `0x01` (GET/SET) |
| 4 | Default Value | 2 | UINT16 | `0x0002` |
| 5 | Current Value | 2 | UINT16 ||
| 6 | Form Flag | 1 | UINT8 | `0x02` (Enumeration) |

### Supported Values

| Value | Description |
|:--|:--|
| `0x0001` | Manual<br>Manually set the aperture via [`0x5007 F-number`](./f_number.md), the ISO sensitivity via [`0x500F ExposureIndex`](./exposure_index.md), and the shutter speed via [`0xD00F ShutterSpeed`](./shutter_speed.md) |
| `0x0002` | Automatic<br>If [`0xD80B Filter`](./filter.md) is enabled, this value is overwritten automatically. |
| `0x0003` | Aperture Priority<sup>\*1</sup><br>Manually set the aperture via [`0x5007 F-number`](./f_number.md).|
| `0x0004` | Shutter Priority<br>Manually set the shutter speed via [`0xD00F ShutterSpeed`](./shutter_speed.md). |
| `0x8003` | ISO Sensitivity Priority<br>Manually set the ISO sensitivity via [`0x500F ExposureIndex`](./exposure_index.md). |

<sup>\*1</sup>Supported by only THETA Z1.  
