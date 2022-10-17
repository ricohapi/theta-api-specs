# 0x501B TimelapseInterval

### Device Prop Code

0x501B

### Overview

Acquire or set the shooting interval (msec) for interval shooting.

This property can be set only when the [StillCaptureMode](still_capture_mode.md) is single shooting.  
Set this property before switching the StillCaptureMode to interval shooting.

### Support model

| X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|
| All | All | All | All | All |

### Support value

This can be set in 1000 msec unit.  
The value that can be set differs depending on the size of the image ([ImageSize](image_size.md)) or the image format ([ImageFormat](image_format.md)) to be shot.

For RICOH THETA Z1 or later

| ImageFormat | Value |
|:--|:--|
| JPEG | Minimum value: 6000<br>Maximum value: 3600000 |
| RAW+ | Minimum value: 10000<br>Maximum value: 3600000 |

For RICOH THETA V

| ImageSize | Value |
|:--|:--|
| 5376 x 2688 | Minimum value: 4000<br>Maximum value: 3600000 |

For RICOH THETA S or SC

| ImageSize | Value |
|:--|:--|
| 5376 x 2688 | Minimum value: 8000<br>Maximum value: 3600000 |
| 2048 x 1024 | Minimum value: 5000<br>Maximum value: 3600000 |
