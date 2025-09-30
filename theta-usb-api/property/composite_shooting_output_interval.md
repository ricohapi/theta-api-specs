# 0xD810 CompositeShootingOutputInterval

**Vendor Extension Property**  
Returns and sets the current setting of the output interval (seconds) for interval composite shooting.  

### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) | ![SC](https://img.shields.io/badge/SC-orange) | ![S](https://img.shields.io/badge/S-red) |
|:-:|:-:|:-:|:-:|:-:|
|   | ✓ |   | ✓<sup>\*1</sup> | ✓<sup>\*2</sup> |

<sup>\*1</sup>THETA SC firmware v1.10 and later  
<sup>\*2</sup>THETA S firmware v1.82 and later  

| Field Order | Field Name | Size | Data Type | Description |
|:-:|:--|:-:|:--|:--|
| 1 | Property Code | 2 | UINT16 | `0xD810` |
| 2 | Datatype | 2 | UINT16 | `0x0006` (UINT32) |
| 3 | Get/Set | 1 | UINT8 | `0x01` (GET/SET) |
| 4 | Default Value | 4 | UINT32 | `0` |
| 5 | Current Value | 4 | UINT32 ||
| 6 | Form Flag | 1 | UINT8 | `0x01` (Range) |
| 7 | Minimum Value | 4 | UINT32 | `0` (No intermediate output) |
| 8 | Maximum Value | 4 | UINT32 | `600` (10 minutes) |
| 9 | Step Size | 4 | UINT32 | `60` (1 minute) |
