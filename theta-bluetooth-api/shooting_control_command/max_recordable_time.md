# Max Recordable Time

### Service

1D0F3602-8DFB-4340-9045-513040DAD991

### Characteristic

6EABAB73-7F2B-4061-BE7C-1D71D143CB7D

### Format

sint16

### Overview

Acquires or sets the maximum recordable time (in seconds) of the camera.

### Value Fields

300, 1500, 3000 (*1)

(*1) THETA Z1 Version 3.01.1 and later, only for 3.6K 1/2fps and 2.7K 1/2fps.  
If you set 3000 seconds in 3.6K 2fps mode and then set back to 4K 30fps mode, the max recordable time will be overwritten to 300 seconds automatically.

### Properties

| Property | Requirement |
|:--|:--|
| Read | Mandatory |
| Write | Mandatory |
| Notify | Excluded |
