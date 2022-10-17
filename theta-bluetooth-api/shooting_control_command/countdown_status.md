# Countdown Status

### Service

1D0F3602-8DFB-4340-9045-513040DAD991

### Characteristic

F399C66A-1D8E-49BF-9420-94AC17D8C20B

### Format

sint8

### Overview

Acquires the camera states in the self-timer mode. Can also instruct the camera to stop self-timer shooting.

### Value Fields

| Value | Description |
|:--|:--|
| 0 | Shooting completed (notification from the camera only) |
| 1 | Self-timer shooting active (notification from the camera only) |
| 2 | Cancel shooting |

### Properties

| Property | Requirement |
|:--|:--|
| Read | Mandatory |
| Write | Mandatory |
| Notify | Mandatory |
