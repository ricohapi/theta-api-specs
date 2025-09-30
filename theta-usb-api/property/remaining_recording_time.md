# 0xD80A RemainingRecordingTime

**Vendor Extension Property**  
Returns the remained video recording time (seconds).  

### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) | ![SC](https://img.shields.io/badge/SC-orange) | ![S](https://img.shields.io/badge/S-red) |
|:-:|:-:|:-:|:-:|:-:|
| ✓ | ✓ | ✓ | ✓ | ✓ |

| Field Order | Field Name | Size | Data Type | Description |
|:-:|:--|:-:|:--|:--|
| 1 | Property Code | 2 | UINT16 | `0xD80A` |
| 2 | Datatype | 2 | UINT16 | `0x0004` (UINT16) |
| 3 | Get/Set | 1 | UINT8 | `0x00` (GET) |
| 4 | Default Value | 2 | UINT16 | `0` |
| 5 | Current Value | 2 | UINT16 ||
| 6 | Form Flag | 1 | UINT8 | `0x01` (Range) |
| 7 | Minimum Value | 2 | UINT16 | `0` |
| 8 | Maximum Value | 2 | UINT16 | `7200` for THETA X<br>`3000` for THETA Z1<br>`1500` for THETA V and S<br>`300` for THETA SC |
| 9 | Step Size | 2 | UINT16 | `1` (1 second) |
