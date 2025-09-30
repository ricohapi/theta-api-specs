# 0xD806 Passphrase

**Vendor Extension Property**  
Returns and sets the current value of the passphrase of wireless LAN direct mode.  

### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) | ![SC](https://img.shields.io/badge/SC-orange) | ![S](https://img.shields.io/badge/S-red) |
|:-:|:-:|:-:|:-:|:-:|
| ✓ | ✓ | ✓ | ✓ | ✓ |

| Field Order | Field Name | Size | Data Type | Description |
|:-:|:--|:-:|:--|:--|
| 1 | Property Code | 2 | UINT16 | `0xD806` |
| 2 | Datatype | 2 | UINT16 | `0xFFFF` (STRING) |
| 3 | Get/Set | 1 | UINT8 | `0x01` (GET/SET) |
| 4 | Default Value | 9 | STRING ||
| 5 | Current Value | 64 | STRING ||
| 6 | Form Flag | 1 | UINT8 | `0x00` (None) |

> [!NOTE]
> * A string with a length between 8 and 63 characters.  
> * Only printable ASCII characters are allowed.  
> * Returns NULL in THETA X firmware v2.71.1 and later, and THETA Z1 firmware v3.30.2 and later.  
