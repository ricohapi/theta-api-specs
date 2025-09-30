# 0xD407 PerceivedDeviceType

Returns the device type.  
In RICOH THETA, this property value is fixed to `0x00000001`.  

### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) | ![SC](https://img.shields.io/badge/SC-orange) | ![S](https://img.shields.io/badge/S-red) |
|:-:|:-:|:-:|:-:|:-:|
| ✓ | ✓ | ✓ | ✓ | ✓ |

| Field Order | Field Name | Size | Data Type | Description |
|:-:|:--|:-:|:--|:--|
| 1 | Property Code | 2 | UINT16 | `0xD407` |
| 2 | Datatype | 2 | UINT16 | `0x0006` (UINT16) |
| 3 | Get/Set | 1 | UINT8 | `0x00` (GET) |
| 4 | Default Value | 2 | UINT16 | `0x00000001` |
| 5 | Current Value | 2 | UINT16 ||
| 6 | Form Flag | 1 | UINT8 | `0x00` (None) |

### Supported Values

| Value | Description |
|:--|:--|
| `0x00000000` | Generic device |
| `0x00000001` | Camera |
