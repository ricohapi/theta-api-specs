# 0xD808 CaptureStatus

### Device Prop Code

0xD808

### Overview

Acquire the camera shooting execution status.  
(Vendor Expansion Properties)

| PropValue | Status |
|:--|:--|
| 0 | Shooting standby status |
| 1 | Executing continuous shooting<br>- Executing interval shooting<br>- Recording video|

### Event

Changes to CaptureStatus are notified by a [DevicePropChanged](../event/device_prop_changed.md) event.
