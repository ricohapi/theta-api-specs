# 0xD81D NetworkType

**Vendor Extension Property**  
Returns or sets the current setting of the network type.  

### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) | ![SC](https://img.shields.io/badge/SC-orange) | ![S](https://img.shields.io/badge/S-red) |
|:-:|:-:|:-:|:-:|:-:|
| ✓ | ✓ | ✓ |   |   |

| Field Order | Field Name | Size | Data Type | Description |
|:-:|:--|:-:|:--|:--|
| 1 | Property Code | 2 | UINT16 | `0xD81D` |
| 2 | Datatype | 2 | UINT8 | `0x0002` (UINT8) |
| 3 | Get/Set | 1 | UINT8 | `0x01` (GET/SET) |
| 4 | Default Value | 1 | UINT8 | `0` |
| 5 | Current Value | 1 | UINT8 ||
| 6 | Form Flag | 1 | UINT8 | `0x02` (Enumeration) |

### Supported Values

| Value | Description |
|:-:|:--|
| `0` | OFF |
| `1` | Direct mode (AP mode) |
| `2` | Client mode (CL mode)<sup>\*1</sup> |

<sup>\*1</sup>For THETA Z1/X, this mode can be enabled when an access point has been set using [`0x99A3 GetAccessPointHandles`](../operation/get_access_point_handles.md).  
