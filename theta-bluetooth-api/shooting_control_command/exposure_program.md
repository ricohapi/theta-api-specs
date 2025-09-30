# Exposure Program

### Service

1D0F3602-8DFB-4340-9045-513040DAD991

### Characteristic

96302827-37D9-4719-A2E3-9234C4F34292

### Format

sint8

### Overview

Acquires and sets the exposure program of the camera.

It can be set for video shooting mode at RICOH THETA V firmware v3.00.1 and later.  
Shooting settings are retained separately for both the Still image shooting mode and Video shooting mode.

### Value Fields

| **Value** | **Description** |
|:--|:--|
| 1 | Manual program<br>[ISO](iso.md), [Shutter Speed](shutter_speed.md) and [Aperture](../shooting_control_command_v2/aperture.md) (RICOH THETA Z1 o r later) can be set manually. |
| 2 | Normal program<br>All exposure settings are automatically configured.<br>This value is used when the [image processing filter](filter.md) is enabled. |
| 3 | Aperture priority program<br>[Aperture](../shooting_control_command_v2/aperture.md) can be manually set.<br>RICOH THETA Z1 and later. |
| 4 | Shutter priority program<br>[Shutter Speed](shutter_speed.md) can be manually set. |
| 9 | ISO priority program<br>[ISO](iso.md) can be manually set. |

### Properties

| Property | Requirement |
|:--|:--|
| Read | Mandatory |
| Write | Mandatory |
| Notify | Excluded |
