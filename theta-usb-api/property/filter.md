# 0xD80B Filter

**Vendor Extension Property**  
Returns and sets the current value of the image processing filter.  

This property is effective only for single-shot still capture mode.  
If the filter is enabled, it takes precedence over the exposure program [`0x500E ExposureProgramMode`](./exposure_program_mode.md). In such cases, the exposure program is forced to Automatic.  

### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) | ![SC](https://img.shields.io/badge/SC-orange) | ![S](https://img.shields.io/badge/S-red) |
|:-:|:-:|:-:|:-:|:-:|
| ✓ | ✓ | ✓ | ✓ | ✓ |

| Field Order | Field Name | Size | Data Type | Description |
|:-:|:--|:-:|:--|:--|
| 1 | Property Code | 2 | UINT16 | `0xD80B` |
| 2 | Datatype | 2 | UINT16 | `0x0002` (UINT8) |
| 3 | Get/Set | 1 | UINT8 | `0x01` (GET/SET) |
| 4 | Default Value | 1 | UINT8 | `0x00` (OFF) |
| 5 | Current Value | 1 | UINT8 ||
| 6 | Form Flag | 1 | UINT8 | `0x02` (Enumeration) |

### Supported Values

| Value | ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) | ![SC](https://img.shields.io/badge/SC-orange) | ![S](https://img.shields.io/badge/S-red) | Description |
|:--|:-:|:-:|:-:|:-:|:-:|:--|
| `0x00` | ✓ | ✓ | ✓ | ✓ | ✓ | OFF |
| `0x01` |   | ✓ | ✓ | ✓ | ✓ | DR Compensation |
| `0x02` | ✓ | ✓<sup>\*4</sup> | ✓ | ✓ | ✓ | Noise Reduction |
| `0x03` | ✓ | ✓<sup>\*4</sup> | ✓ | ✓ | ✓ | HDR |
| `0x04` | ✓<sup>\*1</sup> | ✓<sup>\*2\*4</sup> | ✓<sup>\*3</sup> ||| Handheld HDR |

<sup>\*1</sup>THETA X firmware v2.40.0 and later  
<sup>\*2</sup>THETA Z1 firmware v1.20.1 and later  
<sup>\*3</sup>THETA V firmware v3.10.1 and later  
<sup>\*4</sup>The filter can be configured even when [`0xD827 ImageFormat`](./image_format.md) is set to `0x01` (RAW+) with THETA Z1 firmware v2.00.1 and later  
