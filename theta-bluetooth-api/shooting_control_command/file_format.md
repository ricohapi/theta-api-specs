# File Format

### Service

1D0F3602-8DFB-4340-9045-513040DAD991

### Characteristic

E8F0EDD1-6C0F-494A-95C3-3244AE0B9A01

### Format

sint8

### Overview

Acquires and sets the recording size (pixels) of the camera.

### Value Fields

For RICOH THETA Z1 or later, can be set 1, 3, 6 or 7.

For RICOH THETA V, can be set 0, 1 or 3.

| Value | Description |
|:--|:--|
| 0 | Still image. 5376x2688 |
| 1 | Movie. 3840x1920. H.264/MPEG-4 AVC |
| 2 | Reserved |
| 3 | Movie. 1920x960. H.264/MPEG-4 AVC |
| 4 | Reserved |
| 5 | Reserved |
| 6 | Still image JPEG format. 6720x3360 (Equirectangular) or 7296x3648 (Dual-Fisheye) |
| 7 | Still image RAW+ format. 7296x3648 |

### Properties

| Property | Requirement |
|:--|:--|
| Read | Mandatory |
| Write | Mandatory |
| Notify | Excluded |
