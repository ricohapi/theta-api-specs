# 0x5001 BatteryLevel

Returns the current battery level.  

### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) | ![SC](https://img.shields.io/badge/SC-orange) | ![S](https://img.shields.io/badge/S-red) |
|:-:|:-:|:-:|:-:|:-:|
| ✓ | ✓ | ✓ | ✓ | ✓ |

| Field Order | Field Name | Size | Data Type | Description |
|:-:|:--|:-:|:--|:--|
| 1 | Property Code | 2 | UINT16 | `0x5001` |
| 2 | Datatype | 2 | UINT16 | `0x0002` (UINT8) |
| 3 | Get/Set | 1 | UINT8 | `0x00` (GET) |
| 4 | Default Value | 1 | UINT8 | `100` |
| 5 | Current Value | 1 | UINT8 | `0` to `100`<sup>\*1</sup> |
| 6 | Form Flag | 1 | UINT8 | `0x01` (Range) |
| 7 | Minimum Value | 1 | UINT8 | `0` (0%) |
| 8 | Maximum Value | 1 | UINT8 | `100` (100%) |
| 9 | Step Size | 1 | UINT8 | `1` (1%) |

<sup>\*1</sup>If the device is powered solely by an external power source, the return value is always `100`.  
