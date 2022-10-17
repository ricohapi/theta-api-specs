# Filter

### Service

1D0F3602-8DFB-4340-9045-513040DAD991

### Characteristic

246231F9-176B-48F2-A675-B946D6A46999

### Format

sint8

### Overview

Acquires or sets the image processing filter of the camera.

The filter set in the still image shooting mode is applied.   
The filter is disabled in the interval shooting, interval composite group shooting or multi bracket shooting mode.

When the filter is enabled, it is prioritized over the exposure program ([Exposure Program](exposure_program.md)) setting.   
The exposure program is set to Normal while the filter is enabled.

The condition below will result in an error.

- [File Format](file_format.md) is RAW+ format and \_filter is Noise reduction, HDR or Handheld HDR
- [Shooting Method](../shooting_control_command_v2/shooting_method.md)is except for Normal shooting and \_filter is enabled
- Access duaring video capture mode

### Value Fields

| Value | Description |
|:--|:--|
| 0 | OFF |
| 1 | Noise reduction |
| 2 | HDR |
| 3 | DR compensation |
| 4 | Handheld HDR<br>RICOH THETA Z1 firmware v1.20.1 or later and RICOH THETA V firmware v3.10.1 or later |

### Properties

| Property | Requirement |
|:--|:--|
| Read | Mandatory |
| Write | Mandatory |
| Notify | Excluded |
