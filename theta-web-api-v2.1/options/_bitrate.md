# \_bitrate

### Overview

Movie bit rate.

Can be acquired by [camera.getOptions](../commands/camera.get_options.md) and set by [camera.setOptions](../commands/camera.set_options.md).

### Support model

| X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|
| All | All | v2.50.1 or later | --- | --- |

### Support value

The supported value depends on the shooting mode ([captureMode](capture_mode.md)).

| Shooting mode | Supported value |
|:--|:--|
| video | "Fine", "Normal", "Economy"(RICOH THETA X or later)<br/>"2000000"-"120000000"\*1(RICOH THETA X v1.20 or later) |
| image | "Auto", "1048576"-"20971520"\*2(RICOH THETA X v1.20 or later) |
| _liveStreaming | "Auto" |

\*1 The actual bit rate varies depending on the resolution, frame rate, shooting conditions, subject, etc.  
\*2 Images are treated with the target file size. The actual image file size varies depending on the resolution, shooting conditions, subject, etc.  
