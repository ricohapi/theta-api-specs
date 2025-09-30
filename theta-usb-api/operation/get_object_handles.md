# 0x1007 GetObjectHandles

Returns the ObjectHandle corresponding to the specified storage ID.  

### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) | ![SC](https://img.shields.io/badge/SC-orange) | ![S](https://img.shields.io/badge/S-red) |
|:-:|:-:|:-:|:-:|:-:|
| ✓ | ✓ | ✓ | ✓ | ✓ |

| | |
|:--|:--|
| Operation Code | `0x1007` |
| Operation Parameter 1 | `StorageID` |
| Operation Parameter 2 | `ObjectFormatCode`<sup>\*1</sup> |
| Operation Parameter 3 | `ObjectHandle` of Association<sup>\*1</sup> |
| Operation Parameter 4 | None |
| Operation Parameter 5 | None |
| Data | `ObjectHandle` array<sup>\*2</sup> |
| Data Direction | R->I |

<sup>\*1</sup>Unused. Specify `0x00000000`.  
<sup>\*2</sup>The maximum number of ObjectHandles that can be used is 9,999, including both directories and files.  
