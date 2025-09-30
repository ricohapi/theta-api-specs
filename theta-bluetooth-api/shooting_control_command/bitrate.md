# Bitrate

### Service

1D0F3602-8DFB-4340-9045-513040DAD991

### Characteristic

C94DD895-6FFA-42AC-8454-1315ED21FAAD

### Format

sint8

### Overview

Sets or acquires the movie bit rate of the camera.  
RICOH THETA V firmware v2.50.1 and later.

### Value Fields

The supported value depends on the shooting mode ([Capture Mode](capture_mode.md)).

| Value | Description |
|:--|:--|
| 1 | Normal.<br>In Movie shooting mode only. |
| 2 | High bit rate.<br>In Movie shooting mode only. |
| 0 | Automatic.<br>In still image shooting mode or live streaming mode |

### Properties

| Property | Requirement |
|:--|:--|
| Read | Mandatory |
| Write | Mandatory |
| Notify | Excluded |
