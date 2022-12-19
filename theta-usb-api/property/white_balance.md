# 0x5005 WhiteBalance

### Device Prop Code

0x5005

### Overview

Acquires and sets the white balance.

It can be set for video shooting mode at RICOH THETA V firmware v3.00.1 or later. Shooting settings are retained separately for both the Still image shooting mode and Video shooting mode.

### Support model

| X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|
| All | All | All | All | All |

### Support value

| Value | Description |
|:--|:--|
| 0x0002 | AUTO |
| 0x0004 | Outdoor |
| 0x8001 | Shade |
| 0x8002 | Cloudy |
| 0x0006 | Incandescent light 1 |
| 0x8020 | Incandescent light 2 |
| 0x8003 | Fluorescent light 1 (daylight) |
| 0x8004 | Fluorescent light 2 (natural white) |
| 0x8005 | Fluorescent light 3 (white) |
| 0x8006 | Fluorescent light 4 (light bulb color) |
| 0x8007 | CT settings (specified by [ColorTemperature](color_temperature.md)) \*1 |
| 0x8008 | Underwater \*2 \*3 |

\*1 RICOH THETA S firmware v01.82 or later and RICOH THETA SC firmware v01.10 or later

\*2 RICOH THETA V firmware v3.21.1 or later

\*3 With RICOH THETA X, stitching process will be optimized for underwater setting when 0x5005 WhiteBalance is set to 0x8008 Underwater.
