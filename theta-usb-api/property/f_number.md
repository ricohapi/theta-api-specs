# 0x5007 F-number

Returns and sets the current setting of F-number.  

### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) | ![SC](https://img.shields.io/badge/SC-orange) | ![S](https://img.shields.io/badge/S-red) |
|:-:|:-:|:-:|:-:|:-:|
|   | ✓ |   |   |   |

| Field Order | Field Name | Size | Data Type | Description |
|:-:|:--|:-:|:--|:--|
| 1 | Property Code | 2 | UINT16 | `0x5007` |
| 2 | Datatype | 2 | UINT16 | `0x0004` (UINT16) |
| 3 | Get/Set | 1 | UINT8 | `0x01` (GET/SET) |
| 4 | Default Value | 2 | UINT16 | `0x0000` |
| 5 | Current Value | 2 | UINT16 ||
| 6 | Form Flag | 1 | UINT8 | `0x02` (Enumeration) |

### Supported Values

| Value | Description |
|:--|:--|
| `0x0000` | Automatic |
| `0x0001` | F2.1<sup>\*1<sup> |
| `0x0002` | F3.5<sup>\*1<sup> |
| `0x0003` | F5.6<sup>\*1<sup> |

<sup>\*1</sup>Supported only when the exposure program [`0x500E ExposureProgramMode`](exposure_program_mode.md) is set to `0x0001` Manual or `0x0003` Aperture Priority.  
