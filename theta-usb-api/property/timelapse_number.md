# 0x501A TimelapseNumber

Returns and sets the current setting of the number of shots for interval shooting mode.  

### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) | ![SC](https://img.shields.io/badge/SC-orange) | ![S](https://img.shields.io/badge/S-red) |
|:-:|:-:|:-:|:-:|:-:|
| ✓ | ✓ | ✓ | ✓ | ✓ |

| Field Order | Field Name | Size | Data Type | Description |
|:-:|:--|:-:|:--|:--|
| 1 | Property Code | 2 | UINT16 | `0x501A` |
| 2 | Datatype | 2 | UINT16 | `0x0004` (UINT16) |
| 3 | Get/Set | 1 | UINT8 | `0x01` (GET/SET) |
| 4 | Default Value | 2 | UINT16 | `0x0000` (Unlimited) |
| 5 | Current Value | 2 | UINT16 ||
| 6 | Form Flag | 1 | UINT8 | `0x01` (Range) |
| 7 | Minimum Value | 2 | UINT16 | `0` (Unlimited) |
| 8 | Maximum Value | 2 | UINT16 | `9999` |
| 9 | Step Size | 1 | UINT8 | `1` |

> [!WARNING]
> For THETA S/SC, this property is available only when [`0x5013 StillCaptureMode`](still_capture_mode.md) 
 is `0x0001` (Single-shot shooting). Configure this property prior to changing [`0x5013 StillCaptureMode`](still_capture_mode.md) to `0x0003` (Interval shooting).  
