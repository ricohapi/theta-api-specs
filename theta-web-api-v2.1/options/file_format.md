# fileFormat

### Overview

Image format used in shooting.

Can be acquired by [camera.getOptions](../commands/camera.get_options.md) and set by [camera.setOptions](../commands/camera.set_options.md).

### Support value

The supported value depends on the shooting mode ([captureMode](capture_mode.md)).

#### For RICOH THETA X or later

| Shooting mode | Supported value |
|:--|:--|
| image | {"type": "jpeg","width": 11008,"height": 5504}<br>{"type": "jpeg","width": 5504,"height": 2752} |
| video | {"type": "mp4","width": 7680,"height": 3840, "_codec": "H.264/MPEG-4 AVC", "_frameRate": 10}<br>{“type”: “mp4”,”width”: 7680,”height”: 3840, “_codec”: “H.264/MPEG-4 AVC”, “_frameRate”: 5}<br>{“type”: “mp4”,”width”: 7680,”height”: 3840, “_codec”: “H.264/MPEG-4 AVC”, “_frameRate”: 2}<br>{"type": "mp4","width": 5760,"height": 2880, "_codec": "H.264/MPEG-4 AVC", "_frameRate": 30}<br>{“type”: “mp4”,”width”: 5760,”height”: 2880, “_codec”: “H.264/MPEG-4 AVC”, “_frameRate”: 5}<br>{“type”: “mp4”,”width”: 5760,”height”: 2880, “_codec”: “H.264/MPEG-4 AVC”, “_frameRate”: 2}<br>{"type": "mp4","width": 3840,"height": 1920, "_codec": "H.264/MPEG-4 AVC", "_frameRate": 60}<br>{"type": "mp4","width": 3840,"height": 1920, "_codec": "H.264/MPEG-4 AVC", "_frameRate": 30}<br>{"type": "mp4","width": 1920,"height": 960, "_codec": "H.264/MPEG-4 AVC", "_frameRate": 60}<br>{"type": "mp4","width": 1920,"height": 960, "_codec": "H.264/MPEG-4 AVC", "_frameRate": 30} |
| \_liveStreaming | Not supported |



#### For RICOH THETA Z1

| Shooting mode | Supported value |
|:--|:--|
| image | {"type": "jpeg","width": 6720,"height": 3360}<br>{"type": "raw+","width": 6720,"height": 3360} |
| video | {"type": "mp4", "width": 3840, "height": 1920, "\_codec": "H.264/MPEG-4 AVC"}<br>{"type": "mp4", "width": 1920, "height": 960, "\_codec": "H.264/MPEG-4 AVC"} |
| \_liveStreaming | Not supported |



#### For RICOH THETA V

| Shooting mode | Supported value |
|:--|:--|
| image | {"type": "jpeg", "width": 5376, "height": 2688} |
| video | {"type": "mp4", "width": 3840, "height": 1920, "\_codec": "H.264/MPEG-4 AVC"}<br>{"type": "mp4", "width": 1920, "height": 960, "\_codec": "H.264/MPEG-4 AVC"} |
| \_liveStreaming | Not supported |



#### For RICOH THETA S or SC

| Shooting mode | Supported value |
|:--|:--|
| image | {"type": "jpeg", "width": 5376, "height": 2688}<br>{"type": "jpeg", "width": 2048, "height": 1024} |
| video | {"type": "mp4", "width": 1920, "height": 1080}<br>{"type": "mp4", "width": 1280, "height": 720} |
| \_liveStreaming | Not supported |
