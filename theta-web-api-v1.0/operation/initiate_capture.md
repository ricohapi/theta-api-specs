# 0x100E InitiateCapture

### Operation Code

0x100E

### Overview

Start shooting.

The compatibility status of options is as follows.

| Operation Parameter | RICOH THETA Specification |
|:--|:--|
| StorageID | unused<br>Specify 0x00000000. |
| ObjectFormatCode | unused<br>Specify 0x00000000. |

### Prohibited Operations

If the InitiateCapture operation is requested under any of the following conditions, a DeviceBusy response is notified during processing

- During video shooting or saving (RICOH THETA m15)
- [StillCaptureMode](../property/still_capture_mode.md) is a different mode to single shot mode
- The shooting mode is video shooting mode (RICOH THETA m15)
