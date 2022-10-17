# whiteBalance

### Overview

White balance.

It can be set for video shooting mode at RICOH THETA V firmware v3.00.1 or later. Shooting settings are retained separately for both the Still image shooting mode and Video shooting mode.

Can be acquired by [camera.getOptions](../commands/camera.get_options.md) and set by [camera.setOptions](../commands/camera.set_options.md).

### Support model

| X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|
| All | All | All | All | All |

### Support value

| Value | Description |
|:--|:--|
| auto | Automatic |
| daylight | Outdoor |
| shade | Shade |
| cloudy-daylight | Cloudy |
| incandescent | Incandescent light 1 |
| _warmWhiteFluorescent | Incandescent light 2 |
| _dayLightFluorescent | Fluorescent light 1 (daylight) |
| _dayWhiteFluorescent | Fluorescent light 2 (natural white) |
| fluorescent | Fluorescent light 3 (white) |
| _bulbFluorescent | Fluorescent light 4 (light bulb color) |
| _colorTemperature | CT settings (specified by the <a href="_color_temperature.md">_colorTemperature</a> option) \*1 |
| _underwater | Underwater \*2 |

\*1 RICOH THETA S firmware v01.82 or later and RICOH THETA SC firmware v01.10 or later

\*2 RICOH THETA V firmware v3.21.1 or later
