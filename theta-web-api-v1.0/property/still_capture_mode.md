# 0x5013 StillCaptureMode

### Device Prop Code

0x5013

### Overview

Acquire or set the still image shooting method.  
Return to the default value when the power is turned OFF or when [InitiateOpenCapture](../operation/initiate_open_capture.md) ends.

Setting mode is as follows.

| Prop Value | RICOH THETA Specification |
|:--|:--|
| 0x0000 | Value when the shooting mode is "Video shooting mode".<br>Cannot change to other Still Capture Modes.<br>(RICOH THETA m15) |
| 0x0001 | Single shot mode.<br>Default value when the shooting mode is "Still image shooting mode". |
| 0x0003 | Interval shooting mode.<br>[TimelapseNumber](timelapse_number.md) and [TimelapseInterval](timelapse_interval.md) cannot be changed when this mode is set. Change these setting values before switching to interval shooting mode. |
