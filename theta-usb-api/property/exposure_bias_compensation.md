# 0x5010 ExposureBiasCompensation

Returns and sets the current setting of the exposure compensation.  
This setting is available in video recording mode on RICOH THETA V firmware v3.00.1 and later. Shooting settings are maintained separately for still capture mode and video recording mode.  

### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) | ![SC](https://img.shields.io/badge/SC-orange) | ![S](https://img.shields.io/badge/S-red) |
|:-:|:-:|:-:|:-:|:-:|
| ✓ | ✓ | ✓ | ✓ | ✓ |

| Field Order | Field Name | Size | Data Type | Description |
|:-:|:--|:-:|:--|:--|
| 1 | Property Code | 2 | UINT16 | `0x5010` |
| 2 | Datatype | 2 | UINT16 | `0x0003` (INT16) |
| 3 | Get/Set | 1 | UINT8 | `0x01` (GET/SET) |
| 4 | Default Value | 2 | INT16 | `0` |
| 5 | Current Value | 2 | INT16 ||
| 6 | Form Flag | 1 | UINT8 | `0x02` (Enumeration) |

### Supported Values

The following values are supported when the exposure program ([`0x500E ExposureProgramMode`](./exposure_program_mode.md)) is set to `0x0002` Automatic, `0x0003` Aperture Priority, `0x0004` Shutter Priority, `0x8003` ISO Sensitivity Priority modes. `0x0001` Manual mode supports only `0` (±0Ev).  

| Value | Description |
|:--|:--|
| `2000` | +2.0Ev |
| `1700` | +1.7Ev |
| `1300` | +1.3Ev |
| `1000` | +1.0Ev |
| `700`  | +0.7Ev |
| `300`  | +0.3Ev |
| `0`    | ±0Ev   |
| `-300` | -0.3Ev |
| `-700` | -0.7Ev |
| `-1000` | -1.0Ev |
| `-1300` | -1.3Ev |
| `-1700` | -1.7Ev |
| `-2000` | -2.0Ev |
