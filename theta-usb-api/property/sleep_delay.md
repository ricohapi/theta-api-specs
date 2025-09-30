# 0xD803 SleepDelay

**Vendor Extension Property**  
Returns and sets the current setting of the sleep mode transition time (seconds).  

### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) | ![SC](https://img.shields.io/badge/SC-orange) | ![S](https://img.shields.io/badge/S-red) |
|:-:|:-:|:-:|:-:|:-:|
| ✓ | ✓ | ✓ | ✓ | ✓ |

| Field Order | Field Name | Size | Data Type | Description |
|:-:|:--|:-:|:--|:--|
| 1 | Property Code | 2 | UINT16 | `0xD803` |
| 2 | Datatype | 2 | UINT16 | `0x0004` (UINT16) |
| 3 | Get/Set | 1 | UINT8 | `0x01` (GET/SET) |
| 4 | Default Value | 2 | UINT16 | `300` for THETA SC/S<br>`180` for THETA X/Z1/V |
| 5 | Current Value | 2 | UINT16 | <sup>\*1</sup> |
| 6 | Form Flag | 1 | UINT8 | `0x01` (Range) |
| 7 | Minimum Value | 2| UINT16 | `0` (OFF) |
| 8 | Maximum Value | 2 | UINT16 | `1800` for THETA SC/S<br>`65534` for THETA X/Z1/V<sup>\*1</sup> |
| 9 | Step Size | 2 | UINT16 | `1` (1 second) |

<sup>\*1</sup>If a value between `1` and `59` is specified, it is treated as `60`.  
