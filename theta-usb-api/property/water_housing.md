# 0xD83B WaterHousing

**Vendor Extension Property**  
Returns or sets the current setting of usage underwater hausing to optimize the image processing.  
See also [`0xD83C Water Housing Stitching`](./water_housing_stitching.md).  

### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) | ![SC](https://img.shields.io/badge/SC-orange) | ![S](https://img.shields.io/badge/S-red) |
|:-:|:-:|:-:|:-:|:-:|
| ✓<sup>\*1</sup> |   |   |   |   |

<sup>\*1</sup>THETA X firmware v1.40.0 and later

| Field Order | Field Name | Size | Data Type | Description |
|:-:|:--|:-:|:--|:--|
| 1 | Property Code | 2 | UINT16 | `0xD83B` |
| 2 | Datatype | 2 | UINT16 | `0x0002` (UINT8) |
| 3 | Get/Set | 1 | UINT8 | `0x01` (GET/SET) |
| 4 | Default Value | 1 | UINT8 | `0` |
| 5 | Current Value | 1 | UINT8 ||
| 6 | Form Flag | 1 | UINT8 | `0x02` (None) |

| Value | Description |
|:-:|:--|
| `0` | Not use water housing |
| `1` | Use water housing |
