# 0xD840 hdrBracket

**Vendor Extension Property**  
Gets or sets the current setting of bracket steps for HDR mode.  
This parameter is valid only for HDR mode, not for Handheld HDR mode.  

### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) | ![SC](https://img.shields.io/badge/SC-orange) | ![S](https://img.shields.io/badge/S-red) |
|:-:|:-:|:-:|:-:|:-:|
| ✓<sup>\*1</sup> | ✓<sup>\*2</sup>  |   |   |   |

<sup>\*1</sup>THETA X firmware v2.50.2 and later  
<sup>\*2</sup>THETA Z1 firmware v3.30.2 and later  

| Field Order | Field Name | Size | Data Type | Description |
|:-:|:--|:-:|:--|:--|
| 1 | Property Code | 2 | UINT16 | `0xD840` |
| 2 | Datatype | 2 | UINT16 | `0x0002` (UINT8) |
| 3 | Get/Set | 1 | UINT8 | `0x01` (GET/SET) |
| 4 | Default Value | 1 | UINT8 | `0` |
| 5 | Current Value | 1 | UINT8 ||
| 6 | Form Flag | 1 | UINT8 | `0x02` (Enumeration) |

| Value | Description |
|:-:|:--|
| `0x00` | -4Ev / ±0Ev / +2Ev |
| `0x01` | -1Ev / ±0Ev / +1Ev |
| `0x02` | -2Ev / ±0Ev / +1Ev |
| `0x03` | -3Ev / ±0Ev / +3Ev |
| `0x04` | -4Ev / ±0Ev / +4Ev |
| `0x05` | -5Ev / ±0Ev / +2Ev |
