# exposureProgram

### Overview

Exposure program. The exposure settings that take priority can be selected.

It can be set for video shooting mode at RICOH THETA V firmware v3.00.1 or later. Shooting settings are retained separately for both the Still image shooting mode and Video shooting mode.

The current setting can be acquired by [camera.getOptions](../commands/camera.get_options.md), and it can be changed by [camera.setOptions](../commands/camera.set_options.md).

### Support model

| X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|
| All | All | All | All | All |

### Support value

| Value | Description |
|:--|:--|
| 1 | Manual program<br>Manually set the ISO sensitivity ([iso](iso.md)) setting, shutter speed ([shutterSpeed](shutter_speed.md)) and aperture ([aperture](aperture.md), RICOH THETA Z1). |
| 2 | Normal program<br>Exposure settings are all set automatically. |
| 3 | Aperture priority program<br>Manually set the aperture ([aperture](aperture.md)).<br>(RICOH THETA Z1) |
| 4 | Shutter priority program<br>Manually set the shutter speed ([shutterSpeed](shutter_speed.md)). |
| 9 | ISO priority program<br>Manually set the ISO sensitivity ([iso](iso.md)) setting. |
