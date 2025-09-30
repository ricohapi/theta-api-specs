# 0xD822 CapturedPictures

**Vendor Extension Property**  
Returns the number of captured images in continuous shooting mode.  
This property can be used only when the shooting method [`0x5013 StillCaptureMode`](./still_capture_mode.md) is set to Interval Shooting, Multi-bracket Shooting, or Continuous Shooting.  

### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) | ![SC](https://img.shields.io/badge/SC-orange) | ![S](https://img.shields.io/badge/S-red) |
|:-:|:-:|:-:|:-:|:-:|
| ✓ | ✓ | ✓ |   |   |

| Field Order | Field Name | Size | Data Type | Description |
|:-:|:--|:-:|:--|:--|
| 1 | Property Code | 2 | UINT16 | `0xD822` |
| 2 | Datatype | 1 | UINT8 | `0x0004` (UINT16) |
| 3 | Get/Set | 1 | UINT8 | `0x00` (GET) |
| 4 | Default Value | 2 | UINT16 | `0` |
| 5 | Current Value | 2 | UINT16 ||
| 6 | Form Flag | 1 | UINT8 | `0x00` (None) |
