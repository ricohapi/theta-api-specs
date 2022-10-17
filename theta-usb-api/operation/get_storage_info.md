# 0x1005 GetStorageInfo

### Operation Code

0x1005

### Overview

Return information on the specified storage ID.

Changes in the storage information associated with the change of [ImageSize](../property/image_size.md) property are notified by [StorageInfoChanged](../event/storage_info_changed.md) event.

Details of each Dataset field are as follows.

| Name | RICOH THETA Specification |
|:--|:--|
| MaxCapability | Storage capacity |
| FreeSpaceInBytes | Remaining usable storage space |
| FreeSpaceInImages | Remaining number of shots |

Recalculation of the remaining number of photos that can be recorded is done at one of the following times.

- When the camera power is turned ON
- After storage of an image file is completed
- When changes are made to the number of files or number of directories in the storage
- When [ImageSize](../property/image_size.md) property is changed

### Support model

| X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|
| All | All | All | All | All |
