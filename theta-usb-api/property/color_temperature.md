# 0xD813 ColorTemperature

**Vendor Extension Property**  
Returns or sets the current setting of specified color temperature (Kelvin) in white balance.  
This setting is available in video recording mode on RICOH THETA V firmware v3.00.1 and later. Shooting settings are maintained separately for still capture mode and video recording mode.  

### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) | ![SC](https://img.shields.io/badge/SC-orange) | ![S](https://img.shields.io/badge/S-red) |
|:-:|:-:|:-:|:-:|:-:|
| ✓ | ✓ | ✓ | ✓<sup>\*1</sup> | ✓<sup>\*2</sup> |

<sup>\*1</sup>THETA SC firmware v1.10 and later  
<sup>\*2</sup>THETA S firmware v1.82 and later  

| Field Order | Field Name | Size | Data Type | Description |
|:-:|:--|:-:|:--|:--|
| 1 | Property Code | 2 | UINT16 | `0xD813` |
| 2 | Datatype | 2 | UINT16 | `0x0004` (UINT16) |
| 3 | Get/Set | 1 | UINT8 | `0x01` (GET/SET) |
| 4 | Default Value | 2 | UINT16 | `5000` |
| 5 | Current Value | 2 | UINT16 ||
| 6 | Form Flag | 1 | UINT8 | `0x01` (Range) |
| 7 | Minimum Value | 2 | UINT16 | `2500` (2500 Kelvin) |
| 8 | Maximum Value | 2 | UINT16 | `10000` (10000 Kelvin) |
| 9 | Step Size | 2 | UINT16 | `100` (100 Kelvin) |
