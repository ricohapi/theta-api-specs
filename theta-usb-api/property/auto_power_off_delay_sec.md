# 0xD81B AutoPowerOffDelaySec

**Vendor Extension Property**  
Returns and sets the current setting of the auto power off transition time (seconds).  

### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) | ![SC](https://img.shields.io/badge/SC-orange) | ![S](https://img.shields.io/badge/S-red) |
|:-:|:-:|:-:|:-:|:-:|
| ✓ | ✓ | ✓ |   |   |

Refer to [`0xD802 AutoPowerOffDelay`](./auto_power_off_delay.md) for THETA SC/S.  

| Field Order | Field Name | Size | Data Type | Description |
|:-:|:--|:-:|:--|:--|
| 1 | Property Code | 2 | UINT16 | `0xD81B` |
| 2 | Datatype | 2 | UINT16 | `0x0006` (UINT32) |
| 3 | Get/Set | 1 | UINT8 | `0x01` (GET/SET) |
| 4 | Default Value | 4 | UINT32 | `64800` (18 hours) |
| 5 | Current Value | 4 | UINT32 | <sup>\*1</sup> |
| 6 | Form Flag | 1 | UINT8 | `0x01` (Range) |
| 7 | Minimum Value | 4 | UINT32 | `0` (OFF) |
| 8 | Maximum Value | 4 | UINT32 | `2592000` (30 days) |
| 9 | Step Size | 4 | UINT32 | `60` (1 minute) |

<sup>\*1</sup>If a value between `1` and `599` is specified, it is treated as `600`.  
