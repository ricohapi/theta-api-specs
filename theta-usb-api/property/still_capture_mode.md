# 0x5013 StillCaptureMode

### Device Prop Code

0x5013

### Overview

Acquires or sets the shooting method.

### Support model

| X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|
| All | All | All | All | All |

### Support value

| Value | Description |
|:--|:--|
| 0x0001 | Single-shot shooting<br>Value when the shooting mode is set to "Still Image Shooting". |
| 0x0003 | Interval shooting<br>Can be set when the shooting mode is set to "Still Image Shooting". |
| 0x8002 | Movie shooting<br>Value when the shooting mode is set to "Movie Shooting". |
| 0x8003 | Interval composite shooting \*1\*3\*5<br>Can be set when the shooting mode is set to "Still Image Shooting". |
| 0x8004 | Multi bracket shooting \*1<br>Can be set when the shooting mode is set to "Still Image Shooting". |
| 0x8005 | Live streaming \*2<br>Value when the shooting mode is set to "Live Streaming". |
| 0x8006 | Continuous shooting \*6<br>Can be set when the shooting mode is set to "Still Image Shooting".<br><br>Interval shooting (optimized \*4, Tripod stabilization Off)<br>Can be set when the shooting mode is set to "Still Image Shooting". |
| 0x8007 | Time shift shooting \*6<br>Can be set when the shooting mode is set to "Still Image Shooting".<br><br>Interval shooting (optimized \*4, Tripod stabilization On)<br>Can be set when the shooting mode is set to "Still Image Shooting". |
| 0x8008 | Burst shooting \*7<br>Can be set when the shooting mode is set to "Still Image Shooting". |

\*1 RICOH THETA S firmware v01.82 or later and RICOH THETA SC firmware v1.10 or later

\*2 RICOH THETA V or later

\*3 RICOH THETA V is not supported

\*4 RICOH THETA Z1 v1.50.1 or later and RICOH THETA V firmware v3.40.1 or later<br>Top/bottom correction and stitching conditions are optimized.

\*5 RICOH THETA X is not supported

\*6 RICOH THETA X or later

\*7 RICOH THETA Z1 v2.10.1 or later. Enabled only for RICOH THETA Z1

### Event

When the shooting mode has been changed by operating the camera, a [DevicePropChanged](../event/device_prop_changed.md) event is informed.
