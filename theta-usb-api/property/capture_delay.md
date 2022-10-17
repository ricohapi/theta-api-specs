# 0x5012 CaptureDelay

### Device Prop Code

0x5012

### Overview

Acquire or set the operating time (msec) of the self-timer.  
This property can be set in still image capture mode and in movie shooting mode (RICOH THETA V firmware v2.50.1 or later).

If captureDelay is enabled, self-timer is used by shooting.

### Support model

| X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|
| All | All | v2.50.1 or later | All | All |

### Support value

0 (Disabled), 1000 or over, 10000 or less (Enabled)

This can be set in 1000 msec unit.
