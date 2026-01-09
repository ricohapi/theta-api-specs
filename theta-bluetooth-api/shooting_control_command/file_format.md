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

For RICOH THETA Z1 and later, can be set 1, 3, 6, 7, 9, 11, 13 or 15.

For RICOH THETA V, can be set 0, 1 or 3.

| Value | Description |
|:--|:--|
| `0` | Still image. 5376x2688 |
| `1` | Movie. 3840x1920. H.264/MPEG-4 AVC |
| `2` | Reserved |
| `3` | Movie. 1920x960. H.264/MPEG-4 AVC |
| `4` | Reserved |
| `5` | Reserved |
| `6` | Still image JPEG format. 6720x3360 (Equirectangular) or 7296x3648 (Dual-Fisheye) |
| `7` | Still image RAW+ format. 7296x3648 |
| `9` \*1 | Movie. 2688x2688. H.264/MPEG-4 AVC |
| `11` \*1 | Movie. 3648x3648. H.264/MPEG-4 AVC |
| `13` \*2 | Movie. 2688x2688. H.264/MPEG-4 AVC. Dual video track |
| `15` \*2 | Movie. 3648x3648. H.264/MPEG-4 AVC. Dual video track |

\*1 RICOH THETA Z1 firmware v3.01.1 and later. This mode outputs two fisheye video for each lens. The MP4 file name ending with `_0` is the video file on the front lens, and `_1` is back lens. This mode does not record audio track to MP4 file.  
\*2 RICOH THETA Z1 firmware v3.60.3 and later. This mode outputs one MP4 video file which contains two video tracks. First video track is for the front lens, and second video track is for the back lens.  

### Properties

| Property | Requirement |
|:--|:--|
| Read | Mandatory |
| Write | Mandatory |
| Notify | Excluded |
