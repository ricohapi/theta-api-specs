# 0xD826 IsoAutoHighLimit

Sets and Returns the current setting of the Maximum ISO sensitivity for auto mode.  

### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) | ![SC](https://img.shields.io/badge/SC-orange) | ![S](https://img.shields.io/badge/S-red) |
|:-:|:-:|:-:|:-:|:-:|
| ✓ | ✓ | ✓<sup>\*1</sup> |   |   |

<sup>\*1</sup>THETA V firmware v3.00.1 and later  

| Field Order | Field Name | Size | Data Type | Description |
|:-:|:--|:-:|:--|:--|
| 1 | Property Code | 2 | UINT16 | `0xD826` |
| 2 | Datatype | 2 | UINT16 | `0x0004` (UINT16) |
| 3 | Get/Set | 1 | UINT8 | `0x01` (GET/SET) |
| 4 | Default Value | 2 | UINT16 | `800` for THETA X (5.5K)<br>`1600` for THETA X (11K and video recording mode)<br>`3200` for THETA Z1/V (Still capture mode)<br>`6400` for THETA Z1/V (Video recording mode) |
| 5 | Current Value | 2 | UINT16 ||
| 6 | Form Flag | 1 | UINT8 | `0x02` (Enumeration) |

### Supported Values

The following values are supported when the exposure program ([`0x500E ExposureProgramMode`](./exposure_program_mode.md)) is set to `0x0002` Automatic, `0x0003` Aperture Priority, or `0x0004` Shutter Priority.  

##### THETA X

`100`, `125`, `160`, `200`, `250`, `320`, `400`, `500`, `640`, `800`,  
`1000`, `1250`, `1600`, `2000`, `2500`, `3200`  

#### THETA Z1 and THETA V (Video shooting mode)

`200`, `250`, `320`, `400`, `500`, `640`, `800`,  
`1000`, `1250`, `1600`, `2000`, `2500`, `3200`, `4000`, `5000`, `6400`  

#### THETA V (Still capture mode)

`200`, `250`, `320`, `400`, `500`, `640`, `800`,  
`1000`, `1250`, `1600`, `2000`, `2500`, `3200`  
