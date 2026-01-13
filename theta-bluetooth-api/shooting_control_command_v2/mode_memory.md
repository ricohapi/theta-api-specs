# Mode Memory

### Service

38EF1533-B0CC-4722-B6B6-8B23C27ECE5C

### Characteristic

F3A9C1E2-7B4D-4C8A-9E3F-2D8F6B1A9C3E  

### Format

sint8

### Overview

Mode Memory has been introduced to retain some settings instead of reverting to defaults, when the device enters sleep mode or is powered off.   
This API is available with RICOH THETA Z1 firmware v3.60.3 and later.

### Value Fields

| Value | Description |
|:--|:--|
| `0` | When the device enters sleep mode or is powered off,<br>the following settings **will revert to their default values**. This is default value. |
| `1` | When the device enters sleep mode or is powered off,<br>the following settings **will be retained for the next startup**.  |

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

### Properties

| Property | Requirement |
|:--|:--|
| Read   | Mandatory |
| Write  | Mandatory |
| Notify | Excluded  |
