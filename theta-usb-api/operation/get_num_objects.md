# 0x1006 GetNumObjects

Returns the number of objects associated with the specified storage ID.  

### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) | ![SC](https://img.shields.io/badge/SC-orange) | ![S](https://img.shields.io/badge/S-red) |
|:-:|:-:|:-:|:-:|:-:|
| ✓ | ✓ | ✓ | ✓ | ✓ |

| | |
|:--|:--|
| Operation Code | `0x1006` |
| Operation Parameter 1 | `StorageID` |
| Operation Parameter 2 | `ObjectFormatCode`<sup>\*1</sup> |
| Operation Parameter 3 | `ObjecHandle` of Association<sup>\*1</sup> |
| Operation Parameter 4 | None |
| Operation Parameter 5 | None |
| Data | None |
| Data Direction | N/A |
| Response Parameter 1 | `NumObjects` |
| Response Parameter 2 | None |
| Response Parameter 3 | None |
| Response Parameter 4 | None |
| Response Parameter 5 | None |

<sup>\*1</sup>Unused. Specify `0x00000000`.  
