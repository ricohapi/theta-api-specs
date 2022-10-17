# 0x501A TimelapseNumber

### Device Prop Code

0x501A

### Overview

Acquire or set the upper limit value for interval shooting.   
Shooting is unlimited when 0x0000 is set.  
Return to the default value when the power is turned OFF.

1. This property cannot be set when the [StillCaptureMode](still_capture_mode.md) is interval shooting mode.   
Set this property before switching the StillCaptureMode to interval shooting mode.
1. TimelapseNumber cannot be set or operate when it is 1. Specify as 0 (unlimited), 2 or larger.
