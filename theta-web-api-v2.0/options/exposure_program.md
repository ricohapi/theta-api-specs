# exposureProgram

### Overview

Exposure program. The exposure settings that take priority can be selected.

The current setting can be acquired by [camera.getOptions](../commands/camera.get_options.md), and it can be changed by [camera.setOptions](../commands/camera.set_options.md).

### Support value

| Value | Description |
|:--|:--|
| 1 | Manual program <br>Manually set the ISO sensitivity (<a href="iso.md">iso</a>) setting and shutter speed (<a href="shutter_speed.md">shutterSpeed</a>). |
| 2 | Normal program <br>Exposure settings are all set automatically. |
| 4 | Shutter priority program <br>Manually set the shutter speed (<a href="shutter_speed.md">shutterSpeed</a>). |
| 9 | ISO priority program <br>Manually set the ISO sensitivity (<a href="iso.md">iso</a>) setting. |
