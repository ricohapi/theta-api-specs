# 0x400C StorageInfoChanged

Notification of storage information change ([`0x1005 GetStorageInfo`](../operation/get_storage_info.md)).  
When the image size ([`0x5003 ImageSize`](../property/image_size.md)) is changed, FreeSpaceInImages in the storage information is also updated.  

### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) | ![SC](https://img.shields.io/badge/SC-orange) | ![S](https://img.shields.io/badge/S-red) |
|:-:|:-:|:-:|:-:|:-:|
| ✓ | ✓ | ✓ | ✓ | ✓ |

| | |
|:--|:--|
| Event Code | `0x400C` |
| Parameter 1 | `StorageID` |
| Parameter 2 | None |
| Parameter 3 | None |
