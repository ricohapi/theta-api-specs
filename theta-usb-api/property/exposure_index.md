# 0x500F ExposureIndex

Returns and sets the current setting of the ISO sensitivity.  
This setting is available in video recording mode on RICOH THETA V firmware v3.00.1 and later. Shooting settings are maintained separately for still capture mode and video recording mode.  

### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) | ![SC](https://img.shields.io/badge/SC-orange) | ![S](https://img.shields.io/badge/S-red) |
|:-:|:-:|:-:|:-:|:-:|
| ✓ | ✓ | ✓ | ✓ | ✓ |

| Field Order | Field Name | Size | Data Type | Description |
|:-:|:--|:-:|:--|:--|
| 1 | Property Code | 2 | UINT16 | `0x500F` |
| 2 | Datatype | 2 | UINT16 | `0x0004` (UINT16) |
| 3 | Get/Set | 1 | UINT8 | `0x01` (GET/SET) |
| 4 | Default Value | 2 | UINT16 | `0xFFFF` |
| 5 | Current Value | 2 | UINT16 ||
| 6 | Form Flag | 1 | UINT8 | `0x02` (Enumeration) |

### Supported Values

The following values are supported when the exposure program ([`0x500E ExposureProgramMode`](./exposure_program_mode.md)) is set to `0x0001` Manual or `0x8003` ISO Priority.  

##### THETA X

`50`, `64`, `80`,  
`100`, `125`, `160`, `200`, `250`, `320`, `400`, `500`, `640`, `800`,  
`1000`, `1250`, `1600`, `2000`, `2500`, `3200`  

##### THETA Z1

`80`,  
`100`, `125`, `160`, `200`, `250`, `320`, `400`, `500`, `640`, `800`,  
`1000`, `1250`, `1600`, `2000`, `2500`, `3200`, `4000`, `5000`, `6400`  

##### THETA V

`80`,  
`100`, `125`, `160`, `200`, `250`, `320`, `400`, `500`, `640`, `800`,  
`1000`, `1250`, `1600`, `2000`, `2500`, `3200`, `4000`<sup>\*1</sup>, `5000`<sup>\*1</sup>, `6400`<sup>\*1</sup>  

<sup>\*1</sup>Supported only in video recording mode  

##### THETA SC/S

`100`, `125`, `160`, `200`, `250`, `320`, `400`, `500`, `640`, `800`,  
`1000`, `1250`, `1600`,  

#### Otherwise

`0xFFFF` (Automatic)  
