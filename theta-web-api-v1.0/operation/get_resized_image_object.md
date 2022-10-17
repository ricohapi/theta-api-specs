# 0x1022 GetResizedImageObject

### Operation Code

0x1022

### Overview

An object resized to 2048 x 1024 pixels is acquired for the specified object handle.   
Operation parameters are as follows.

| No. | Operation Parameter | RICOH THETA Specification |
|:--|:--|:--|
| 1 | ObjectHandle | Acquisition Target Object Handle |
| 2 | image width in pixels | Specify 2048. |
| 3 | image height in pixels | Specify 1024. |
| 4 | Reserved | Specify 0. |
| 5 | Reserved | Specify 0. |

GetResizedImageObject replies DeviceBusy during video shooting or saving.
