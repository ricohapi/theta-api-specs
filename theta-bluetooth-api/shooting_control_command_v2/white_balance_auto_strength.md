# White Balance Auto Strength

### Service

38EF1533-B0CC-4722-B6B6-8B23C27ECE5C

### Characteristic

5328A0CC-254D-460A-89F5-E8ED7D2EFFC1

### Format

sint8

### Overview

To set the strength of white balance auto for low color temperature scene. This parameter can be set for photo mode and video mode separately. Also this parameter will not be cleared by power-off.  
This API is available with RICOH THETA Z1 firmware v2.20.3 or later.

### Value Fields

| Value | Description |
|:--|:--|
| 0 | not correct tint for low color temperature scene (default) |
| 1 |     correct tint for low color temperature scene |

### Properties

| Property | Requirement |
|:--|:--|
| Read   | Mandatory |
| Write  | Mandatory |
| Notify | Excluded  |
