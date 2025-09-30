# 0xD81F Gain

**Vendor Extension Property**  
Returns or sets the current setting of the microphone gain.  

### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) | ![SC](https://img.shields.io/badge/SC-orange) | ![S](https://img.shields.io/badge/S-red) |
|:-:|:-:|:-:|:-:|:-:|
| ✓ | ✓ | ✓ |   |   |

| Field Order | Field Name | Size | Data Type | Description |
|:-:|:--|:-:|:--|:--|
| 1 | Property Code | 2 | UINT16 | `0xD81F` |
| 2 | Datatype | 2 | UINT8 | `0x0002` (UINT8) |
| 3 | Get/Set | 1 | UINT8 | `0x01` (GET/SET) |
| 4 | Default Value | 1 | UINT8 | `0` |
| 5 | Current Value | 1 | UINT8 ||
| 6 | Form Flag | 1 | UINT8 | `0x02` (Enumeration) |

### Supported Values

| Value | Description |
|:-:|:--|
| `0x00` | Normal gain |
| `0x01` | Low gain for a loud environment |
| `0x02` | Mute<sup>\*1\*2</sup> |

<sup>\*1</sup>THETA V firmware v2.50.1 and later  
<sup>\*2</sup>THETA X firmware v2.50.2 and later. The audio track is not recorded in the video file.  
