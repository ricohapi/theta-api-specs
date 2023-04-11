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
| video | "Fine", "Normal", "Economy"(RICOH THETA X or later) \*1<br/>"2000000"-"120000000" (RICOH THETA X v1.20 or later) \*2 |
| image | "Auto", "1048576"-"20971520"\*2(RICOH THETA X v1.20 or later) \*3 |
| _liveStreaming | "Auto" |

----

\*1 Bitrate setting  
RICOH THETA X
| Video mode | Fine<br/>[Mbps] | Normal<br/>[Mbps] | Economy<br/>[Mbps] | Remark
|:--|:--|:--|:--|:--|
|   2K 30fps |  32 |  16 |   8 ||
|   2K 60fps |  64 |  32 |  16 ||
|   4K 10fps |  48 |  24 |  12 ||
|   4K 15fps |  64 |  32 |  16 ||
|   4K 30fps | 100 |  54 |  32 ||
|   4K 60fps | 120 |  64 |  32 ||
| 5.7K  2fps |  16 |  12 |   8 | firmware v2.00.0 or later   |
|            |  64 |  32 |  16 | firmware v1.40.0 or later   (I-frame only)|
|            |  16 |   8 |   4 | firmware v1.30.0 or earlier |
| 5.7K  5fps |  40 |  30 |  20 | firmware v2.00.0 or later   |
|            | 120 |  80 |  40 | firmware v1.40.0 or later   (I-frame only)|
|            |  32 |  16 |   8 | firmware v1.30.0 or earlier |
| 5.7K 10fps |  80 |  60 |  40 | firmware v2.00.0 or later   |
|            |  64 |  40 |  20 | firmware v1.40.0 or later   |
|            |  48 |  24 |  12 | firmware v1.30.0 or earlier |
| 5.7K 15fps |  64 |  32 |  16 ||
| 5.7K 30fps | 120 |  64 |  32 ||
|   8K  2fps |  64 |  32 |  16 | firmware v1.40.0 or later   (I-frame only)|
|            |  32 |  16 |   8 | firmware v1.30.0 or earlier (I-frame only)|
|   8K  5fps | 120 |  96 |  40 | firmware v1.40.0 or later   (I-frame only)|
|            |  64 |  32 |  16 | firmware v1.30.0 or earlier (I-frame only)|
|   8K 10fps | 120 |  96 |  40 | firmware v1.40.0 or later   (I-frame only)|
|            | 120 |  64 |  32 | firmware v1.30.0 or earlier (I-frame only)|

\*2 The actual bit rate varies depending on the resolution, frame rate, shooting conditions, subject, etc.  
\*3 Images are treated with the target file size. The actual image file size varies depending on the resolution, shooting conditions, subject, etc.  
