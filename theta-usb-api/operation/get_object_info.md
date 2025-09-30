# 0x1008 GetObjectInfo

Returns the object information for the specified object handle.  
For EXIF/JPEG data, a 17-byte group ID is returned in the keywords field. This may be one of the following:

* Interval shooting group ID
* Interval composite group shooting ID (17 bytes; supported by THETA Z1, and by THETA S with firmware version 1.82 and later, and THETA SC with firmware version 1.10 and later)
* Multi-bracket shooting group ID (17 bytes; supported by THETA X, THETA Z1, THETA V, and by THETA S with firmware version 1.82 and later, and THETA SC with firmware version 1.10 and later)
* Continious shooting group ID (17 bytes; supported by THETA X)

> [!NOTE]
> Duplicate group IDs may be recorded in the following cases:  
> * The camera's date/time settings were incorrect
> * The camera was used in different time zones

### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) | ![SC](https://img.shields.io/badge/SC-orange) | ![S](https://img.shields.io/badge/S-red) |
|:-:|:-:|:-:|:-:|:-:|
| ✓ | ✓ | ✓ | ✓ | ✓ |

| | |
|:--|:--|
| Operation Code | `0x1008` |
| Operation Parameter 1 | `ObjectHandle` |
| Operation Parameter 2 | None |
| Operation Parameter 3 | None |
| Operation Parameter 4 | None |
| Operation Parameter 5 | None |
| Data | `ObjectInfo` dataset |
| Data Direction | R->I |
