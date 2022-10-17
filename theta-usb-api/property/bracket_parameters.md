# 0xD812 BracketParameters

### Device Prop Code

0xD812

### Overview

Acquires or sets the multi bracket shooting setting.  
(Vendor Extension Property)

### Support model

| X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|
| All | All | All | v1.10 or later | v01.82 or later |

### Support value

The multi bracket shooting setting format is a 16-byte array as defined below (AINT128).

#### For RICOH THETA X or later

The array size should be 2 to 13.

First element: \<ExposureBiasCompensation\>\<ExposureIndex\>\<ShutterSpeed\>\<F-number\>\<ExposureProgramMode\>  
Second element: \<Reserved 96 bits\>\<ColorTemperature\>\<Reserved 16 bits\>

#### For RICOH THETA V firmware v3.00.1 or later

The array size should be 2 to 19.

First element: \<ExposureBiasCompensation\>\<ExposureIndex\>\<ShutterSpeed\>\<F-number\>\<ExposureProgramMode\>  
Second element: \<Reserved 96 bits\>\<ColorTemperature\>\<WhiteBalance\>

#### For RICOH THETA V firmware v2.50.1 or prior

The array size should be 2 to 13.

\<Reserved 32 bits\>\<ColorTemperature\>\<ExposureIndex\>\<ShutterSpeed\>

| Field | Bit length | Description |
|:--|:--|:--|
| ColorTemperature | 16 bits | Color temperature setting<br>Refer to [0xD813 ColorTemperature](color_temperature.md) for the format. |
| ExposureIndex | 16 bits | ISO sensitivity<br>Refer to [0x500F ExposureIndex](exposure_index.md) for the format. |
| ShutterSpeed | 64 bits | Shutter speed<br>Refer to [0xD00F ShutterSpeed](shutter_speed.md) for the format. |
| ExposureBiasCompensation | 16 bits | Exposure compensation<br>Refer to [0x5010 ExposureBiasCompensation](exposure_bias_compensation.md) for the format. |
| F-number | 16 bits | Aperture<br>Refer to [0x5007 F-Number](f_number.md) for the format.<br>Set 0 for RICOH THETA V, X. |
| ExposureProgramMode | 16 bits | Exposure program<br>Refer to [0x500E ExposureProgramMode](exposure_program_mode.md) for the format. |
| WhiteBalance | 16 bits | White balance<br>Refer to [0x5005 WhiteBalance](white_balance.md) for the format. |
