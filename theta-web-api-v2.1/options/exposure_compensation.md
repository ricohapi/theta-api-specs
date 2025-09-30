# exposureCompensation

### Overview

Exposure compensation (EV).

It can be set for video shooting mode at RICOH THETA V firmware v3.00.1 and later. Shooting settings are retained separately for both the Still image shooting mode and Video shooting mode.

The current setting can be acquired by [camera.getOptions](../commands/camera.get_options.md), and it can be changed by [camera.setOptions](../commands/camera.set_options.md).

### Support model

| X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|
| All | All | All | All | All |

### Support value

-2.0, -1.7, -1.3, -1.0, -0.7, -0.3, 0.0, 0.3, 0.7, 1.0, 1.3, 1.7, 2.0

0 if the exposure program ([exposureProgram](exposure_program.md)) is set to Manual Program.
