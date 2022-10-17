# fileFormat

### Overview

Shot image format.

The current setting can be acquired by [camera.getOptions](../commands/camera.get_options.md), and it can be changed by [camera.setOptions](../commands/camera.set_options.md).

### Support value

Values that can be set differ depending on the shooting mode ([captureMode](capture_mode.md)).

| Shooting mode | Support value |
|:--|:--|
| image | {"type": "jpeg", "width": 5376, "height": 2688}<br>{"type": "jpeg", "width": 2048, "height": 1024} |
| \_video | {"type": "mp4", "width": 1920, "height": 1080}<br>{"type": "mp4", "width": 1280, "height": 720} |
| \_liveStreaming | Not supported |
