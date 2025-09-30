# 0x5011 DateTime

Returns and sets the current setting of the date and time.  

### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) | ![SC](https://img.shields.io/badge/SC-orange) | ![S](https://img.shields.io/badge/S-red) |
|:-:|:-:|:-:|:-:|:-:|
| ✓ | ✓ | ✓ | ✓ | ✓ |

| Field Order | Field Name | Size | Data Type | Description |
|:-:|:--|:-:|:--|:--|
| 1 | Property Code | 2 | UINT16 | `0x5011` |
| 2 | Datatype | 2 | UINT16 | `0xFFFF` (STRING) |
| 3 | Get/Set | 1 | UINT8 | `0x01` (GET/SET) |
| 4 | Default Value | 16 | STRING ||
| 5 | Current Value | 16 | STRING ||
| 6 | Form Flag | 1 | UINT8 | `0x00` (None) |

### Format of Current Value

`YYYYMMDD` + `"T"` + `hhmmss` + `{"Z"|"±hhmm"}`  
e.g. `20250901T170030+0900`, `20250901T170030Z`  

> [!NOTE]
> If decimal (fractional) seconds are included, all digits after the decimal point must be discarded (rounded down) when setting the time.  
