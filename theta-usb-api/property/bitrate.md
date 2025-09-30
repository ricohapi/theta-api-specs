# 0xD829 Bitrate

**Vendor Extension Property**  
Returns the current value of the bitrate setting for video recording and still capture.  

### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) | ![SC](https://img.shields.io/badge/SC-orange) | ![S](https://img.shields.io/badge/S-red) |
|:-:|:-:|:-:|:-:|:-:|
| ✓ | ✓ | ✓<sup>\*1</sup> |   |   |

<sup>\*1</sup>THETA V firmware v2.50.1 and later  

| Field Order | Field Name | Size | Data Type | Description |
|:-:|:--|:-:|:--|:--|
| 1 | Property Code | 2 | UINT16 | `0xD829` |
| 2 | Datatype | 2 | UINT16 | `0x0004` (UINT16) |
| 3 | Get/Set | 1 | UINT8 | `0x01` (GET/SET) |
| 4 | Default Value | 2 | UINT16 | `0x0001` for THETA X (Video recording mode)<br>`0x0002` for THETA X (Still Capture mode )<br>`0x0002` for THETA Z1/V (Video recording mode)<br>`0x0000` for THETA Z1/V (Still Capture mode) |
| 5 | Current Value | 2 | UINT16 ||
| 6 | Form Flag | 1 | UINT8 | `0x02` (Enumeration) |

### Supported Values

#### THETA X Video Recording Mode

| Value | Description |
|:--|:--|
| `0x0001` | Normal  |
| `0x0002` | Fine    |
| `0x0003` | Economy |

| Video mode | Fine<br/>[Mbps] | Normal<br/>[Mbps] | Economy<br/>[Mbps] | Remark
|:--|:--|:--|:--|:--|
|   2K 30fps |  32 |  16 |   8 ||
|   2K 60fps |  64 |  32 |  16 ||
|   4K 10fps |  48 |  24 |  12 ||
|   4K 15fps |  64 |  32 |  16 ||
|   4K 30fps | 100 |  54 |  32 ||
|   4K 60fps | 120 |  64 |  32 ||
| 5.7K  2fps |  16 |  12 |   8 | firmware v2.00.0 and later   |
|            |  64 |  32 |  16 | firmware v1.40.0 and later   (I-frame only)|
|            |  16 |   8 |   4 | firmware v1.30.0 or earlier |
| 5.7K  5fps |  40 |  30 |  20 | firmware v2.00.0 and later   |
|            | 120 |  80 |  40 | firmware v1.40.0 and later   (I-frame only)|
|            |  32 |  16 |   8 | firmware v1.30.0 or earlier |
| 5.7K 10fps |  80 |  60 |  40 | firmware v2.00.0 and later   |
|            |  64 |  40 |  20 | firmware v1.40.0 and later   |
|            |  48 |  24 |  12 | firmware v1.30.0 or earlier |
| 5.7K 15fps |  64 |  32 |  16 ||
| 5.7K 30fps | 120 |  64 |  32 ||
|   8K  2fps |  64 |  32 |  16 | firmware v1.40.0 and later   (I-frame only)|
|            |  32 |  16 |   8 | firmware v1.30.0 or earlier (I-frame only)|
|   8K  5fps | 120 |  96 |  40 | firmware v1.40.0 and later   (I-frame only)|
|            |  64 |  32 |  16 | firmware v1.30.0 or earlier (I-frame only)|
|   8K 10fps | 120 |  96 |  40 | firmware v1.40.0 and later   (I-frame only)|
|            | 120 |  64 |  32 | firmware v1.30.0 or earlier (I-frame only)|

#### THETA X Still Capture Mode

| Value | Description |
|:--|:--|
| `0x0002` | Fine |

#### THETA Z1/V Video Recording Mode

| Value | Description |
|:--|:--|
| `0x0001` | Normal |
| `0x0002` | Fine   |

#### THETA Z1/V Still Capture Mode

| Value | Description |
|:--|:--|
| `0x0000` | Automatic |
