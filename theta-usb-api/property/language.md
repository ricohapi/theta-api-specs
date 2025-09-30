# 0xD820 Language

**Vendor Extension Property**  
Returns or sets the current setting of language used in camera OS.  

### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) | ![SC](https://img.shields.io/badge/SC-orange) | ![S](https://img.shields.io/badge/S-red) |
|:-:|:-:|:-:|:-:|:-:|
| ✓ | ✓ | ✓ |   |   |

| Field Order | Field Name | Size | Data Type | Description |
|:-:|:--|:-:|:--|:--|
| 1 | Property Code | 2 | UINT16 | `0xD820` |
| 2 | Datatype | 2 | UINT8 | `0x0002` (UINT8) |
| 3 | Get/Set | 1 | UINT8 | `0x01` (GET/SET) |
| 4 | Default Value | 1 | UINT8 | `0x00` |
| 5 | Current Value | 1 | UINT8 ||
| 6 | Form Flag | 1 | UINT8 | `0x02` (Enumeration) |

### Supported Values

| Value | Description |
|:-:|:--|
| `0x00` | `en-US` American English |
| `0x01` | `en-GB` British English |
| `0x02` | `ja` Japanese |
| `0x03` | `fr` French |
| `0x04` | `de` German |
| `0x05` | `zh-TW` Traditional Chinese |
| `0x06` | `zh-CN` Simplified Chinese |
| `0x07` | `it` Italian |
| `0x08` | `ko` Korean |
