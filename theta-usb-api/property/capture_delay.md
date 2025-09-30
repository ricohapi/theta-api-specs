# 0x5012 CaptureDelay

Returns and sets the current setting of the delay time (msec) for the self-timer.  
This setting is available in video recording mode on RICOH THETA V firmware v3.00.1 and later. Shooting settings are maintained separately for still capture mode and video recording mode.  

### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) | ![SC](https://img.shields.io/badge/SC-orange) | ![S](https://img.shields.io/badge/S-red) |
|:-:|:-:|:-:|:-:|:-:|
| ✓ | ✓ | ✓ | ✓ | ✓ |

| Field Order | Field Name | Size | Data Type | Description |
|:-:|:--|:-:|:--|:--|
| 1 | Property Code | 2 | UINT16 | `0x5012` |
| 2 | Datatype | 2 | UINT16 | `0x0006` (UINT32) |
| 3 | Get/Set | 1 | UINT8 | `0x01` (GET/SET) |
| 4 | Default Value | 4 | UINT32 | `0` |
| 5 | Current Value | 4 | UINT32 ||
| 6 | Form Flag | 1 | UINT8 | `0x01` (Range) |
| 7 | Minimum Value | 4 | UINT32 | `0` (0 sec) |
| 8 | Maximum Value | 4 | UINT32 | `10000` (10 sec)<sup>\*1</sup> |
| 9 | Step Size | 1 | UINT8 | `1000` (1 sec) |

<sup>\*1</sup>The maximum value is `0` when the device is set to live streaming mode.  
