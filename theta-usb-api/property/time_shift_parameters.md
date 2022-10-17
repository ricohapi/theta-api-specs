# 0xD833 TimeShiftParameters

### Device Prop Code

0xD833

### Overview

Settings of Time Shift shooting conditions.  
Set shooting order for front and rear, time to first shot and time to second shot.  
(Vendor Extension Property)

### Support model

| X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|
| All | --- | --- | --- | --- |

### Support value

Configure each setting value with bit fields.   

| bit | Description |
|:--|:--|
| 0-7 | Time (sec) before 1st lens shooting. 0-10 |
| 8-15 | Time (sec) from 1st lens shooting until start of 2nd lens shooting. 0-10 |
| 16 | 0:Shoot from front(side with logo) side after shooting from rear(side with monitor) side.<br/>1:Shoot from rear side after shooting from front side. |
