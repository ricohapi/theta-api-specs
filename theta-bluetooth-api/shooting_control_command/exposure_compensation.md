# Exposure Compensation

### Service

1D0F3602-8DFB-4340-9045-513040DAD991

### Characteristic

30BCC8EB-725D-4048-A832-E76AE26A57E9

### Format

sint8

### Overview

Acquires and sets the EV compensation value of the camera.

It can be set for video shooting mode at RICOH THETA V firmware v3.00.1 and later. Shooting settings are retained separately for both the Still image shooting mode and Video shooting mode.

### Value Fields

0 if the exposure program ([Exposure Program](exposure_program.md)) is set to Manual Program.

| Value | Description |
|:--|:--|
| -6 | -2.0 |
| -5 | -1.7 |
| -4 | -1.3 |
| -3 | -1.0 |
| -2 | -0.7 |
| -1 | -0.3 |
| 0 | 0.0 |
| 1 | 0.3 |
| 2 | 0.7 |
| 3 | 1.0 |
| 4 | 1.3 |
| 5 | 1.7 |
| 6 | 2.0 |

### Properties

| Property | Requirement |
|:--|:--|
| Read | Mandatory |
| Write | Mandatory |
| Notify | Excluded |
