# 0xD816 Password

**Vendor Extension Property**  
Returns or sets the current setting of the password for digest authentication.  
Digest authentication is available only when [`0xD81D NetworkType`](./network_type.md) is `2` client mode.  

### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) | ![SC](https://img.shields.io/badge/SC-orange) | ![S](https://img.shields.io/badge/S-red) |
|:-:|:-:|:-:|:-:|:-:|
| ✓ | ✓ | ✓<sup>\*1</sup> |   |   |

<sup>\*1</sup>THETA V firmware v2.00.2 and later  

| Field Order | Field Name | Size | Data Type | Description |
|:-:|:--|:-:|:--|:--|
| 1 | Property Code | 2 | UINT16 | `0xD816` |
| 2 | Datatype | 2 | UINT8 | `0xFFFF` (STRING) |
| 3 | Get/Set | 1 | UINT8 | `0x01` (GET/SET) |
| 4 | Default Value | 9 | STRING | serial number (e.g. `00123456`)<sup>\*2</sup> |
| 5 | Current Value | 64 | STRING ||
| 6 | Form Flag | 1 | UINT8 | `0x00` (None) |

> [!NOTE]
> * A string with a length between 8 and 63 characters.  
> * Only printable ASCII characters are allowed.  
> * <sup>\*2</sup> In THETA X firmware v2.50.2 and later, or in THETA Z1 firmware v3.30.2 and later, no default password is set. Therefore, digest authentication cannot be used until a password has been configured at least once.
