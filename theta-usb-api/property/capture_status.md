# 0xD808 CaptureStatus

**Vendor Extension Property**  
Returns the current capture status.  

### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) | ![SC](https://img.shields.io/badge/SC-orange) | ![S](https://img.shields.io/badge/S-red) |
|:-:|:-:|:-:|:-:|:-:|
| ✓ | ✓ | ✓ | ✓ | ✓ |

| Field Order | Field Name | Size | Data Type | Description |
|:-:|:--|:-:|:--|:--|
| 1 | Property Code | 2 | UINT16 | `0xD808` |
| 2 | Datatype | 2 | UINT16 | `0x0002` (UINT8) |
| 3 | Get/Set | 1 | UINT8 | `0x00` (GET) |
| 4 | Default Value | 2 | UINT16 | `0x02` |
| 5 | Current Value | 2 | UINT16 ||
| 6 | Form Flag | 1 | UINT8 | `0x02` (Enumeration) |

### Supported Values

| Value | Description |
|:--|:--|
| `0x00` | Standby for shooting |
| `0x01` | Shooting in progress<br><li>Interval shooting<li>Interval Composite shooting<li>Time Shift shooting<li>Continuous shooting<li>Video recording |
| `0x02` | Self-timer in operation |
| `0x03` | Shooting in progress<li>Multi Bracket shooting |
| `0x04` | Video Conversion post processing in progress |
