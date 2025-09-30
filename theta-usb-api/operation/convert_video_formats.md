# 0x99A7 ConvertVideoFormats

**Vendor Extension Operation**  
Converts the format of a saved video file.  

### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) | ![SC](https://img.shields.io/badge/SC-orange) | ![S](https://img.shields.io/badge/S-red) |
|:-:|:-:|:-:|:-:|:-:|
| ✓ | ✓<sup>\*1</sup> | ✓<sup>\*2</sup> |   |   |

<sup>\*1</sup>Firmware v1.31.1 and later  
<sup>\*2</sup>Firmware v3.21.1 and later  

| | |
|:--|:--|
| Operation Code | `0x99A7` |
| Operation Parameter 1 | `ObjectHandle` of saved video file |
| Operation Parameter 2 | None |
| Operation Parameter 3 | None |
| Operation Parameter 4 | None |
| Operation Parameter 5 | None |
| Data | `ConvertVideoFormat` dataset |
| Data Direction | I->R |

### ConvertVideoFormat Dataset

#### THETA X

| Field Order | Field Name | Size | Data Type | Description |
|:-:|:--|:-:|:--|:--|
| 1 | Size | 1 | UINT8 | `1`: 3840x1920 |

> [!NOTE]
> THETA X only supports the conversion from 5760x2880px 30/15/10fps Equirectangular video down-scale to 3840x1920px.  

#### THETA V/Z1

| Field Order | Field Name | Size | Data Type | Description |
|:-:|:--|:-:|:--|:--|
| 1 | Size | 1 | UINT8 | `0`: 1920x960<br>`1`: 3840x1920 |
| 2 | Projection Type | 1 | UINT8 | `0`: Equirectangular |
| 3 | Codec | 1 | UINT8 | `0`: H.264/MPEG-4 AVC |
| 4 | Top Bottom Correction | 1 | UINT8 | `0`: Apply<br>`1`: ApplyFixedDirection<br>`2`: Disapply |
