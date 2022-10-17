# \_captureInterval

### Overview

Shooting interval (sec.) for interval shooting.

The current setting can be acquired by [camera.getOptions](../commands/camera.get_options.md), and it can be changed by [camera.setOptions](../commands/camera.set_options.md).

### Support value

The value that can be set differs depending on the size of the image ([fileFormat](file_format.md)) to be shot.

| Image size | Support value |
|:--|:--|
| 5376 x 2688 | Minimum value (minInterval): 8<br>Maximum value (maxInterval): 3600 |
| 2048 x 1024 | Minimum value (minInterval): 5<br>Maximum value (maxInterval): 3600 |
