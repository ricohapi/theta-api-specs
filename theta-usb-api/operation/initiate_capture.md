# 0x100E InitiateCapture

### Operation Code

0x100E

### Overview

Start shooting.

When [CaptureDelay](../property/capture_delay.md) is enabled, shooting with self-timer is started.

The compatibility status of options is as follows.

| Operation Parameter | RICOH THETA Specification |
|:--|:--|
| StorageID | unused<br>Specify 0x00000000 |
| ObjectFormatCode | unused<br>Specify 0x00000000 |

### Support model

| X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|
| All | All | All | All | All |

### Prohibited Operations

If the InitiateCapture operation is requested under any of the following conditions, a DeviceBusy response is notified during processing.

- During video shooting or saving
- [StillCaptureMode](../property/still_capture_mode.md) is a different mode to single shot mode
