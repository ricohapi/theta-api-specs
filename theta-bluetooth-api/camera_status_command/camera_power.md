# Camera Power

### Service

8AF982B1-F1FF-4D49-83F0-A56DB4C431A7

### Characteristic

B58CE84C-0666-4DE9-BEC8-2D27B27B3211

### Format

sint8

### Overview

Acquires or sets the camera's start-up status.  
When the camera is turned off or put to sleep, it is necessary to reauthorize from [Auth Bluetooth Device](../bluetooth_control_command/auth_bluetooth_device.md).

### Value Fields

| Value | Description |
|:--|:--|
| 0 | Off |
| 1 | On |
| 2 | Sleep |

### Properties

| Property | Requirement |
|:--|:--|
| Read | Mandatory |
| Write | Mandatory |
| Notify | Mandatory |
