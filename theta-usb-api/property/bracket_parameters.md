# 0xD812 BracketParameters

**Vendor Extension Property**  
Returns or sets the current setting for the multi bracket shooting.  

### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) | ![SC](https://img.shields.io/badge/SC-orange) | ![S](https://img.shields.io/badge/S-red) |
|:-:|:-:|:-:|:-:|:-:|
| ✓ | ✓ | ✓ | ✓<sup>\*1</sup> | ✓<sup>\*2</sup> |

<sup>\*1</sup>THETA SC firmware v1.10 and later  
<sup>\*2</sup>THETA S firmware v1.82 and later  

| Field Order | Field Name | Size | Data Type | Description |
|:-:|:--|:-:|:--|:--|
| 1 | Property Code | 2 | UINT16 | `0xD812` |
| 2 | Datatype | 2 | UINT16 | `0x400A` (AINT128) |
| 3 | Get/Set | 1 | UINT8 | `0x01` (GET/SET) |
| 4 | Default Value | 16\*{1|2}\*N | AINT128 | `NULL` |
| 5 | Current Value | 16\*{1|2}\*N | AINT128 ||
| 6 | Form Flag | 1 | UINT8 | `0x00` (None) |

### Format of Current Value

#### THETA X

For each capture setting, two data units of 128 bytes are required.  
The array length `N` must be between 2 and 13.  

First 128 byte  

| Field Order | Field Name | Size | Data Type | Description |
|:-:|:--|:-:|:--|:--|
| 1 | `ExposureBiasCompensation` | 2 | INT16  | [`0x5010 ExposureBiasCompensation`](./exposure_bias_compensation.md) |
| 2 | `ExposureIndex`            | 2 | UINT16 | [`0x500F ExposureIndex`](./exposure_index.md) |
| 3 | `ShutterSpeed`             | 8 | UINT64 | [`0xD00F ShutterSpeed`](./shutter_speed.md) |
| 4 | `F-number`                 | 2 | UINT16 | [`0x5007 F-number`](./f_number.md) |
| 5 | `ExposureProgramMode`      | 2 | UINT16 | [`0x500E ExposureProgramMode`](./exposure_program_mode.md) |

Second 128 byte  

| Field Order | Field Name | Size | Data Type | Description |
|:-:|:--|:-:|:--|:--|
| 1 | Reserved           | 12 | -- | `0x00` |
| 2 | `ColorTemperature` | 2 | UINT16 | [`0xD813 ColorTemperature`](./color_temperature.md) |
| 3 | Reserved           | 2 | -- | `0x00` |

#### THETA Z1, and V firmware v3.00.1 and later

For each capture setting, two data units of 128 bytes are required.  
The array length `N` must be between 2 and 19.  

| Field Order | Field Name | Size | Data Type | Description |
|:-:|:--|:-:|:--|:--|
| 1 | `ExposureBiasCompensation` | 2 | INT16  | [`0x5010 ExposureBiasCompensation`](./exposure_bias_compensation.md) |
| 2 | `ExposureIndex`            | 2 | UINT16 | [`0x500F ExposureIndex`](./exposure_index.md) |
| 3 | `ShutterSpeed`             | 4 | UINT64 | [`0xD00F ShutterSpeed`](./shutter_speed.md) |
| 4 | `F-number`                 | 2 | UINT16 | [`0x5007 F-number`](./f_number.md) |
| 5 | `ExposureProgramMode`      | 2 | UINT16 | [`0x500E ExposureProgramMode`](./exposure_program_mode.md) |

Second 128 byte  

| Field Order | Field Name | Size | Data Type | Description |
|:-:|:--|:-:|:--|:--|
| 1 | Reserved           | 12 | -- | `0x00` |
| 2 | `ColorTemperature` | 2 | UINT16 | [`0xD813 ColorTemperature`](./color_temperature.md) |
| 3 | `WhiteBalance`     | 2 | UINT16 | [`0x5005 WhiteBalance`](./white_balance.md) |

#### THETA V firmware v2.50.1 and earlier

The array length `N` must be between 2 and 13.  

| Field Order | Field Name | Size | Data Type | Description |
|:-:|:--|:-:|:--|:--|
| 1 | Reserved | 4 | -- | `0x00` |
| 2 | `ColorTemperature` | 2 | UINT16 | [`0xD813 ColorTemperature`](./color_temperature.md) |
| 3 | `ExposureIndex`    | 2 | UINT16 | [`0x500F ExposureIndex`](./exposure_index.md) |
| 4 | `ShutterSpeed`     | 8 | UINT64 | [`0xD00F ShutterSpeed`](./shutter_speed.md) |
