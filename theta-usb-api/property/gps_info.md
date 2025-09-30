# 0xD801 GpsInfo

**Vendor Extension Property**  
Returns and sets the current value of GPS information.  

### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) | ![SC](https://img.shields.io/badge/SC-orange) | ![S](https://img.shields.io/badge/S-red) |
|:-:|:-:|:-:|:-:|:-:|
| ✓ | ✓ | ✓ | ✓ | ✓ |

| Field Order | Field Name | Size | Data Type | Description |
|:-:|:--|:-:|:--|:--|
| 1 | Property Code | 2 | UINT16 | `0xD801` |
| 2 | Datatype | 2 | UINT16 | `0xFFFF` (STRING) |
| 3 | Get/Set | 1 | UINT8 | `0x01` (GET/SET) |
| 4 | Default Value | 1 | STRING | `\0` |
| 5 | Current Value | 60 | STRING ||
| 6 | Form Flag | 1 | UINT8 | `0x00` (None) |

### Format of Current Value

`latitude`,`longitude` `altitude`m@`date-time` `timezone`,`datum`  
e.g. `35.681236,139.767125 12.50m@20250904T103045.0 +0900,WGS84`  

| Field Name | Format | Description |
|:--|:--|:--|
| `latitude` | "{\|-}nn.mmmmmm" | [-90.000000, 90.000000] |
| `longitude` | "{\|-}nnn.mmmmmm" | [-180.000000, 180.000000] |
| `altitude` | "{+\|-}nnnn.mm" | [m] |
| `date-time` | "YYYYMMDDThhmmss{\|.s}" | Fractional seconds shall be ignored. |
| `timezone` | "{+\|-}hhmm" or "Z" | "Z" means UTC |
| `datum` | "WGS84" | Only WGS84 is supported |

> [!TIP]
> If a null character is set, the previously configured GPS information will be deleted.  
