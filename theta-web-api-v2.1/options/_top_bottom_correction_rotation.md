# _topBottomCorrectionRotation

### Overview

Sets the front position for the top/bottom correction.  
Enabled only for [_topBottomCorrection](../options/_top_bottom_correction.md) Manual.

The current setting can be acquired by [camera.getOptions](../commands/camera.get_options.md), and it can be changed by [camera.setOptions](../commands/camera.set_options.md).

### Support model

| X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|
| v1.20.0 or later | --- | --- | --- | --- |

### Support value

| Name | Description |
|:--|:--|
| pitch | Specifies the pitch. <br>Specified range is -90.0 to +90.0, stepSize is 0.1 |
| roll | Specifies the roll. <br>Specified range is -180.0 to +180.0, stepSize is 0.1 |
| yaw | Specifies the yaw. <br>Specified range is -180.0 to +180.0, stepSize is 0.1 |

### Example
#### RICOH THETA X
~~~
_topBottomCorrectionRotation: {
    "pitch":"0.0", "roll":"0.0", "yaw":"0.0"
}
~~~
