# 0x5010 ExposureBiasCompensation

### Device Prop Code

0x5010

### Overview

Acquire or set the exposure compensation value.

It can be set for video shooting mode at RICOH THETA V firmware v3.00.1 or later. Shooting settings are retained separately for both the Still image shooting mode and Video shooting mode.

### Support model

| X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|
| All | All | All | All | All |

### Support value

#### When [ExposureProgramMode](exposure_program_mode.md) is normal program, aperture priority program, shutter priority program or ISO priority program

2000 (+2.0) , 1700 (+1.7) , 1300 (+1.3) , 1000 (+1.0) , 700 (+0.7) ,  
300 (+0.3) , 0 (±0) , -300 (-0.3) , -700 (-0.7) , -1000 (-1.0) ,  
-1300 (-1.3) , -1700 (-1.7) , -2000 (-2.0)

#### When [ExposureProgramMode](exposure_program_mode.md) is manual program

0 (±0)
