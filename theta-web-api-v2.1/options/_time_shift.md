# \_timeShift

### Overview

Time shift shooting.

Can be acquired by [camera.getOptions](../commands/camera.get_options.md) and set by [camera.setOptions](../commands/camera.set_options.md).

### Support model

| X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|
| All | All | v3.00.1 and later | --- | --- |

### Support value

| Key | Description |
| --- | --- |
| firstShooting | Shooting order.<br>"front": Shoot from rear side (side with monitor) after shooting from front side (side with logo). "rear": Shoot from front side after shooting from rear side.<br>Default is "front". |
| firstInterval | Time (sec) before 1st lens shooting.<br>0 to 10.<br>For V or Z1, default is 5. For X, default is 2. |
| secondInterval | Time (sec) from 1st lens shooting until start of 2nd lens shooting.<br>0 to 10.<br>Default is 5. |
