# 0x500E ExposureProgramMode

### Device Prop Code

0x500E

### Overview

Acquire or set the exposure program.  
The exposure settings that take priority can be selected.

It can be set for video shooting mode at RICOH THETA V firmware v3.00.1 or later. Shooting settings are retained separately for both the Still image shooting mode and Video shooting mode.

### Support model

| X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|
| All | All | All | All | All |

### Support value

| Value | Description |
|:--|:--|
| 0x0001 | Manual program<br>Manually set the ISO sensitivity ([ExposureIndex](exposure_index.md)) setting, shutter speed ([ShutterSpeed](shutter_speed.md)) and aperture ([F-number](f_number.md), RICOH THETA Z1 o r later). |
| 0x0002 | Normal program<br>Exposure settings are all set automatically.<br>If [Filter](filter.md) is enabled, ExposureProgramMode is set to this value. |
| 0x0003 | Aperture priority program<br>Manually set the aperture ([F-number](f_number.md)).<br>RICOH THETA Z1 only. |
| 0x0004 | Shutter priority program<br>Manually set the shutter speed ([ShutterSpeed](shutter_speed.md)). |
| 0x8003 | ISO priority program<br>Manually set the ISO sensitivity ([ExposureIndex](exposure_index.md)) setting. |
