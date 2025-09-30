# iso

### Overview

ISO sensitivity.

It can be set for video shooting mode at RICOH THETA V firmware v3.00.1 and later. Shooting settings are retained separately for both the Still image shooting mode and Video shooting mode.

Can be acquired by [camera.getOptions](../commands/camera.get_options.md) and set by [camera.setOptions](../commands/camera.set_options.md).

### Support model

| X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|
| All | All | All | All | All |

### Support value

#### When the exposure program ([exposureProgram](exposure_program.md)) is set to Manual or ISO Priority

##### For RICOH THETA X and later

50, 64, 80, 100, 125, 160, 200, 250, 320, 400, 500, 640, 800, 1000, 1250, 1600, 2000, 2500, 3200

##### For RICOH THETA Z1

80, 100, 125, 160, 200, 250, 320, 400, 500, 640, 800, 1000, 1250, 1600, 2000, 2500, 3200, 4000, 5000, 6400

##### For RICOH THETA V

64, 80, 100, 125, 160, 200, 250, 320, 400, 500, 640, 800, 1000, 1250, 1600, 2000, 2500, 3200, 4000\*, 5000\*, 6000\*

\* Available in video shooting mode.

##### For RICOH THETA S or SC

100, 125, 160, 200, 250, 320, 400, 500, 640, 800, 1000, 1250, 1600

#### Otherwise

0 (AUTO)
