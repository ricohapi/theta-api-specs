# 0x500F ExposureIndex

### Device Prop Code

0x500F

### Overview

Acquires or sets the ISO sensitivity.

It can be set for video shooting mode at RICOH THETA V firmware v3.00.1 or later. Shooting settings are retained separately for both the Still image shooting mode and Video shooting mode.

### Support model

| X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|
| All | All | All | All | All |

### Support value

#### When the exposure program ([ExposureProgramMode](exposure_program_mode.md)) is set to Manual or ISO Priority

##### For RICOH THETA X

50, 64, 80, 100, 125, 160, 200, 250, 320, 400, 500, 640, 800, 1000, 1250, 1600, 2000, 2500, 3200

##### For RICOH THETA Z1

80, 100, 125, 160, 200, 250, 320, 400, 500, 640, 800, 1000, 1250, 1600, 2000, 2500, 3200, 4000, 5000, 6400

##### For RICOH THETA V

64, 80, 100, 125, 160, 200, 250, 320, 400, 500, 640, 800, 1000, 1250, 1600, 2000, 2500, 3200, 4000\*, 5000\*, 6000\*

\* Available in Video shooting mode.

##### For RICOH THETA S or SC

100, 125, 160, 200, 250, 320, 400, 500, 640, 800, 1000, 1250, 1600

#### Otherwise

0xFFFF (AUTO)
