# 0xD823 MaxRecordableTime

### Device Prop Code

0xD823

### Overview

Acquires or sets the maximum shooting time (sec) of the camera.  
(Vendor Extension Property)

### Support model

| X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|
| All | All | All | --- | --- |

### Support value

300, 1500, 3000 (\*1), 7200 (\*2)

(*1) THETA Z1 Version 3.01.1 or later, only for 3.6K 1/2fps and 2.7K 1/2fps.  
If you set 3000 seconds in 3.6K 2fps mode and then set back to 4K 30fps mode, the max recordable time will be overwritten to 300 seconds automatically.

(*2) THETA X Version 2.00.0 or later, only for 5.7K 2/5/10fps, 8K 2/5/10fps, and 2.7K\*2.7K 2/5/10fps.  
If you set 7200 seconds in 8K 10fps mode and then set back to 4K 30fps mode, the max recordable time will be overwritten to 1500 seconds automatically.
