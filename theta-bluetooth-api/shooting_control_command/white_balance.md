# White Balance

### Service

1D0F3602-8DFB-4340-9045-513040DAD991

### Characteristic

2361F4FF-2C7E-4FC5-876B-F9B0EFBC06FD

### Format

sint8

### Overview

Acquires and sets the white balance of the camera.

It can be set for video shooting mode at RICOH THETA V firmware v3.00.1 and later. Shooting settings are retained separately for both the Still image shooting mode and Video shooting mode.

### Value Fields

| Value | **Description** |
|:--|:--|
| 0 | auto<br>Automatic |
| 1 | daylight<br>Outdoor |
| 2 | shade<br>Shade |
| 3 | cloudy-daylight<br>Cloudy |
| 4 | incandescent<br>Incandescent light 1 |
| 5 | warmWhiteFluorescent<br>Incandescent light 2 |
| 6 | dayLightFluorescent<br>Fluorescent light 1 (daylight) |
| 7 | dayWhiteFluorescent<br>Fluorescent light 2 (natural white) |
| 8 | fluorescent<br>Fluorescent light 3 (white) |
| 9 | bulbFluorescent<br>Fluorescent light 4 (light bulb color) |
| 10 | color temperature<br>[CT settings](color_temperature.md) |
| 11 | underwater \* |

\* RICOH THETA V firmware v3.21.1 and later

### Properties

| Property | Requirement |
|:--|:--|
| Read | Mandatory |
| Write | Mandatory |
| Notify | Excluded |
