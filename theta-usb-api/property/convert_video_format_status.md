# 0xD831 ConvertVideoFormatStatus

### Device Prop Code

0xD831

### Overview

Acquires progress rate of conversion and information of converted video.  
(Vendor Extension Property)

### Support model

| X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|
| All | v1.31.1 or later | v3.21.1 or later | --- | --- |

### Support value

| Value | Description |
|:--|:--|
| ProgressRate:%d | Conversion is processing.<br>%d is progress rate. |
| ProgressRate:100_ObjectHandle:%d_ObjectSize:%d | Conversion is completed. |
| ProgressRate:000 | Conversion is canceled. |
