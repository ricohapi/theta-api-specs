# Read WLAN Password State

### Service

F37F568F-9071-445D-A938-5441F2E82399

### Characteristic

E522112A-5689-4901-0803-0520637DC895

### Format

sint8

### Overview

Read the setting status of WLAN password (AP mode).

### Value Fields

| Value | Description |
|:--|:--|
| `0` | The WLAN password has not been changed and the initial password is a part of the Theta’s serial number. |
| `1` | The WLAN password has not been changed and the initial password is a random string. |
| `2` | The WLAN password has been changed. |

### Properties

| Property | Requirement |
|:--|:--|
| Read | Mandatory |
| Write | Excluded |
| Notify | Excluded |
