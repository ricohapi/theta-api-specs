# 0xD837 CameraMode

**Vendor Extension Property**  
Returns or sets the current value of the camera screen.  

### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) | ![SC](https://img.shields.io/badge/SC-orange) | ![S](https://img.shields.io/badge/S-red) |
|:-:|:-:|:-:|:-:|:-:|
| ✓ |   |   |   |   |

| Field Order | Field Name | Size | Data Type | Description |
|:-:|:--|:-:|:--|:--|
| 1 | Property Code | 2 | UINT16 | `0xD837` |
| 2 | Datatype | 2 | UINT16 | `0x0004` (UINT16) |
| 3 | Get/Set | 1 | UINT8 | `0x01` (GET/SET) |
| 4 | Default Value | 2 | UINT16 | `0x0001` |
| 5 | Current Value | 2 | UINT16 ||
| 6 | Form Flag | 1 | UINT8 | `0x02` (Enumeration) |

### Supported Values

| Value | Description |
|:--|:--|
| `0x0001` | Shooting screen |
| `0x0002` | Playback screen |
| `0x0003` | Setting screen |
| `0x0004` | Plugin selection screen |

> [!NOTE]  
> SET method supports only `0x0001` (Shooting screen)  
