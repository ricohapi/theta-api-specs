# 0xD808 CaptureStatus

### Device Prop Code

0xD808

### Overview

Acquires the shooting status of the camera.   
(Vendor Extension Property)

### Support model

| X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|
| All | All | All | All | All |

### Support value

| Value | Description |
|:--|:--|
| 0x00 | Standby for shooting |
| 0x01 | Continuously shoots in progress<br>- Interval shooting in progress<br>- Interval composite shooting in progress (RICOH THETA S firmware v01.82 or later and RICOH THETA SC firmware v1.10 or later, RICOH THETA V is not supported, RICOH THETA X is not supported)<br>- Time shift shooting in progress (RICOH THETA V firmware v3.00.1 or later)<br>- Performing movie shooting<br>- Continuous shooting (RICOH THETA X or later) |
| 0x02 | Self-timer is operating |
| 0x03 | Multi bracket shooting in progress (RICOH THETA S firmware v01.82 or later and RICOH THETA SC firmware v1.10 or later) |
| 0x04 | File post-conversion in progress (RICOH THETA V or later) |
