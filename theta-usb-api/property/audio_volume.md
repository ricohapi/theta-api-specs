# 0x502C AudioVolume

Returns and sets the current setting of the audio volume (%), e.g. shutter sound volume.  

### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) | ![SC](https://img.shields.io/badge/SC-orange) | ![S](https://img.shields.io/badge/S-red) |
|:-:|:-:|:-:|:-:|:-:|
| ✓ | ✓ | ✓ | ✓ | ✓ |

| Field Order | Field Name | Size | Data Type | Description |
|:-:|:--|:-:|:--|:--|
| 1 | Property Code | 2 | UINT16 | `0x502C` |
| 2 | Datatype | 2 | UINT16 | `0x0006` (UINT32) |
| 3 | Get/Set | 1 | UINT8 | `0x01` (GET/SET) |
| 4 | Default Value | 4 | UINT32 | `100` |
| 5 | Current Value | 4 | UINT32 ||
| 6 | Form Flag | 1 | UINT8 | `0x01` (Range) |
| 7 | Minimum Value | 4 | UINT32 | `0` (0%) |
| 8 | Maximum Value | 4 | UINT32 | `100` (100%) |
| 9 | Step Size | 4 | UINT32 | `1` (1%) |
