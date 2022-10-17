# \_shootingMethod

### Overview

Shooting method for My Settings mode. In RICOH THETA X, it is used outside of MySetting.
Can be acquired and set only when in the Still image shooting mode and \_function is the My Settings shooting function.  
Changing \_function initializes the setting details to Normal shooting.

Can be acquired by [camera.getOptions](../commands/camera.get_options.md) and set by [camera.setOptions](../commands/camera.set_options.md).

### Support model

| X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|
| All | All | --- | --- | --- |

### Support value

| Key | Description |
|:--|:--|
| normal | Normal shooting |
| interval | Interval shooting |
| moveInterval | Move interval shooting (RICOH THETA Z1 firmware v1.50.1 or later, RICOH THETA X is not supported) |
| fixedInterval | Fixed interval shooting (RICOH THETA Z1 firmware v1.50.1 or later, RICOH THETA X is not supported) |
| bracket | Multi bracket shooting |
| composite | Interval composite shooting (RICOH THETA X is not supported) |
| continuous | Continuous shooting (RICOH THETA X or later) |
| timeShift | TimeShift shooting (RICOH THETA X or later) |
| burst | Burst shooting (RICOH THETA Z1 v2.10.1 or later, RICOH THETA X is not supported) |
