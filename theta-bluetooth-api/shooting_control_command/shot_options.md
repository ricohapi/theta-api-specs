# Shot Options

### Service

1D0F3602-8DFB-4340-9045-513040DAD991

### Characteristic

25EE1173-0196-4DA0-AD4E-474D7E704E01

### Overview

Acquire or set shooting parameters of camera at once.

### Value Fields

| Name | Type | Description |
|:--|:--|:--|
| Capture Mode | sint8 | Action mode of the camera.<br>See [Capture Mode](capture_mode.md) about parameters in detail.<br>Do not set both Movie shooting mode and Filter ON at once |
| Exposure Program | sint8 | Exposure program of the camera.<br>See [Exposure Program](exposure_program.md) about parameters in detail. |
| ISO | sint16 | ISO sensitivity.<br>See [ISO](iso.md) about parameters in detail. |
| Shutter Speed | sint8 | Shutter speed setting of the camera.<br>See [Shutter Speed](shutter_speed.md) about parameters in detail. |
| White Balance | sint8 | White balance of the camera.<br>See [White Balance](white_balance.md) about parameters in detail. |
| Color Temperature | sint16 | Color temperature (Kelvin) of the camera.<br>See [Color Temperature](color_temperature.md) about parameters in detail. |
| Exposure Compensation | sint8 | EV compensation value of the camera.<br>See [Exposure Compensation](exposure_compensation.md) about parameters in detail. |
| File Format | sint8 | Recording size (pixels) of the camera.<br>See [File Format](file_format.md) about parameters in detail. |
| Filter | sint8 | Image processing filter of the camera.<br>See [Filter](filter.md) about parameters in detail.<br>Do not set both Movie shooting mode and Filter ON at once |
| Exposure Delay \* | sint8 | Self-timer time.<br>See [Exposure Delay](exposure_delay.md) about parameters in detail. |
| Aperture \* | sint8 | Aperture.<br>See [Aperture](../shooting_control_command_v2/aperture.md) about parameters in detail. |
| Iso Auto High Limit \* | sint16 | ISO sensitivity upper limit when ISO sensitivity is set to automatic.<br>See [Iso Auto High Limit](../shooting_control_command_v2/iso_auto_high_limit.md) about parameters in detail. |

\* RICOH THETA Z1 and RICOH THETA V firmware v3.00.1 or later

### Properties

| Property | Requirement |
|:--|:--|
| Read | Mandatory |
| Write | Mandatory |
| Notify | Excluded |
