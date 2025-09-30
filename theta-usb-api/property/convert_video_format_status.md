# 0xD831 ConvertVideoFormatStatus

**Vendor Extension Property**  
Returns the progress rate of the video format conversion post-processing.  

### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) | ![SC](https://img.shields.io/badge/SC-orange) | ![S](https://img.shields.io/badge/S-red) |
|:-:|:-:|:-:|:-:|:-:|
| ✓ | ✓<sup>\*1</sup> | ✓<sup>\*2</sup> |   |   |

<sup>\*1</sup>THETA Z1 firmware v1.31.1 and later  
<sup>\*2</sup>THETA V firmware v3.21.1 and later  

| Field Order | Field Name | Size | Data Type | Description |
|:-:|:--|:-:|:--|:--|
| 1 | Property Code | 2 | UINT16 | `0xD831` |
| 2 | Datatype | 2 | UINT16 | `0xFFFF` (STRING) |
| 3 | Get/Set | 1 | UINT8 | `0x00` (GET) |
| 4 | Default Value | 16 | STRING | `ProgressRate:000` |
| 5 | Current Value | 1 | STRING ||
| 6 | Form Flag | 1 | UINT8 | `0x02` (Enumeration) |

### Supported Values

| Value | Description |
|:--|:--|
| `ProgressRate:%d` | Video format conversion is processing.<br>`%d` is progress rate (000-099). |
| `ProgressRate:100_ObjectHandle:%d_ObjectSize:%d` | Video format conversion is completed. |
| `ProgressRate:000` | Video format conversion is canceled. |
