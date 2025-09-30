# 0xD81A MicrophoneChannel

**Vendor Extension Property**  
Returns or sets the current setting of the microphone channels.  

### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) | ![SC](https://img.shields.io/badge/SC-orange) | ![S](https://img.shields.io/badge/S-red) |
|:-:|:-:|:-:|:-:|:-:|
| ✓ | ✓ | ✓ |   |   |

| Field Order | Field Name | Size | Data Type | Description |
|:-:|:--|:-:|:--|:--|
| 1 | Property Code | 2 | UINT16 | `0xD81A` |
| 2 | Datatype | 2 | UINT8 | `0x0002` (UINT8) |
| 3 | Get/Set | 1 | UINT8 | `0x01` (GET/SET) |
| 4 | Default Value | 1 | UINT8 | `1` for THETA X<br>`0` for THETA Z1/V |
| 5 | Current Value | 1 | UINT8 ||
| 6 | Form Flag | 1 | UINT8 | `0x02` (Enumeration) |

### Supported Values

| Value | Description |
|:-:|:--|
| `0` | 360 degree spatial audio + monaural (4ch+1ch)<sup>\*1</sup> |
| `1` | Monaural (1ch) |

<sup>\*1</sup>Not supported by THETA X  
