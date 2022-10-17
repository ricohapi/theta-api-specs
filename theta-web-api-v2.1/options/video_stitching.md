# videoStitching

### Overview

Video stitching during shooting.

The current setting can be acquired by [camera.getOptions](../commands/camera.get_options.md), and it can be changed by [camera.setOptions](../commands/camera.set_options.md).

### Aupport model

| X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|
| All | All | All | --- | --- |

### Support value

| Value | Description |
|:--|:--|
| none | Stitching is OFF.<br>Recorded video is saved in Dual-Fisheye format. |
| ondevice | Stitching by the camera is ON.<br>Recorded video is saved in Equirectangular format. |
