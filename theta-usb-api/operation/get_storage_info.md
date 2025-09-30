# 0x1005 GetStorageInfo

Returns information for the specified storage ID.  
If the [`0x5003 ImageSize`](../property/image_size.md) property changes and it affects the storage information, a [`0x400C StorageInfoChanged`](../event/storage_info_changed.md) event is triggered to notify the update.  

### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) | ![SC](https://img.shields.io/badge/SC-orange) | ![S](https://img.shields.io/badge/S-red) |
|:-:|:-:|:-:|:-:|:-:|
| ✓ | ✓ | ✓ | ✓ | ✓ |

| | |
|:--|:--|
| Operation Code | `0x1005` |
| Operation Parameter 1 | `StorageID` |
| Operation Parameter 2 | None |
| Operation Parameter 3 | None |
| Operation Parameter 4 | None |
| Operation Parameter 5 | None |
| Data | `StorageInfo` dataset |
| Data Direction | R->I |

### StorageInfo Dataset

| Field Order | Field Name | Size | Data Type | Description |
|:-:|:--|:-:|:--|:--|
| 1 | `Storage Type` | 2 | UINT16 ||
| 2 | `Filesystem Type` | 2 | UINT16 ||
| 3 | `Access Capability` | 2 | UINT16 ||
| 4 | `Max Capability` | 8 | UINT64 | Total storage capacity |
| 5 | `Free Space In Bytes` | 8 | UINT64 | Remaining available storage capacity |
| 6 | `Free Space In Objects`<sup>\*1</sup> | 4 | UINT32 | Remaining shot count |
| 7 | `Storage Description` | Variable | String ||
| 8 | `Volume Identifier` | Variable | String ||

<sup>\*1</sup>The remaining number of photos that can be recorded is recalculated at the following times:  

* When the camera is powered on
* After an image file is saved
* When the number of files or directories in the storage changes
* When the [`0x5003 ImageSize`](../property/image_size.md) property is modified
