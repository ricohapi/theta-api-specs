# 0xD833 TimeShiftParameters

**Vendor Extension Property**  
Returns or sets the current setting of Time Shift shooting.  

### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) | ![SC](https://img.shields.io/badge/SC-orange) | ![S](https://img.shields.io/badge/S-red) |
|:-:|:-:|:-:|:-:|:-:|
| ✓ |   |   |   |   |

| Field Order | Field Name | Size | Data Type | Description |
|:-:|:--|:-:|:--|:--|
| 1 | Property Code | 2 | UINT16 | `0xD833` |
| 2 | Datatype | 2 | UINT16 | `0x0006` (UINT32) |
| 3 | Get/Set | 1 | UINT8 | `0x01` (GET/SET) |
| 4 | Default Value | 4 | UINT32 | `0x0000_0502` |
| 5 | Current Value | 4 | UINT32 ||
| 6 | Form Flag | 1 | UINT8 | `0x00` (None) |

### Current Value

Configure each setting using bit fields.  

| Bit | Description |
|:--|:--|
| 0–7  | **Range**: `0`–`10` Time (seconds) before the first lens shoots. |
| 8–15 | **Range**: `0`–`10` Time (seconds) between the first and second lens shooting. |
| 16   | `0`: Shooting starts with the front lens, then the rear lens.<br>`1`: Shooting starts with the rear lens, then the front lens. |
