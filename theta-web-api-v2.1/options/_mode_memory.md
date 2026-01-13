# \_modeMemory

### Overview

Mode Memory has been introduced to retain some settings instead of reverting to defaults, when the device enters sleep mode or is powered off.

Can be acquired by [camera.getOptions](../commands/camera.get_options.md) and set by [camera.setOptions](../commands/camera.set_options.md).

### Support model

| X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|
| -- | v3.60.3 and later | -- | -- | -- |

### Support value

| Value | Description |
|:--|:--|
| `off` | When the device enters sleep mode or is powered off,<br>the following settings **will revert to their default values**. This is default value. |
| `on`  | When the device enters sleep mode or is powered off,<br>the following settings **will be retained for the next startup**. |

- Still image stitching process
- Exposure program / Aperture / Shutter speed / ISO sensitivity / Exposure compensation
- White balance mode / Color temperature setting
- Filters
- Interval shooting: number of shots / interval
- Multi-bracket shooting: number of shots / parameters
- Interval composite shooting: total shooting time / output interval
- Time-shift shooting settings (excluding shooting order)
- Burst shooting options
- Geotag data

> [!NOTE]  
> THETA X and A1 always retain these settings.  
