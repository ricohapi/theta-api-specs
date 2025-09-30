# 0x1004 GetStorageIDs

Returns a list of storage IDs that are currently valid.  

### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) | ![SC](https://img.shields.io/badge/SC-orange) | ![S](https://img.shields.io/badge/S-red) |
|:-:|:-:|:-:|:-:|:-:|
| ✓ | ✓ | ✓ | ✓ | ✓ |

| | |
|:--|:--|
| Operation Code | `0x1004` |
| Operation Parameter 1 | None |
| Operation Parameter 2 | None |
| Operation Parameter 3 | None |
| Operation Parameter 4 | None |
| Operation Parameter 5 | None |
| Data | `StorageID` array |
| Data Direction | R->I |

### Data

| Field Order | Field Name | Size | Data Type | Description |
|:-:|:--|:-:|:--|:--|
| 1 | `StorageID` array | Variable | AUINT32 | The most-significant 16 bits identify a physical storage ID. The least-significant 16 bits identify a logical partition of that physical storage. |

| Physical Storage ID | Logical Storage ID |
|:--|:--|
| `0x0001`: SD memory card | `0x0001`: An SD memory card can be used. |
| `0x0001`: SD memory card | `0x0000`: An SD memory card cannot be used. |
| `0x0002`: Internal memory | `0x0001`: Internal memory can be used. |
| `0x0002`: Internal memory | `0x0000`: Internal memory cannot be used. |
