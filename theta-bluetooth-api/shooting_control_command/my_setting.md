# My Setting

### Service

1D0F3602-8DFB-4340-9045-513040DAD991

### Characteristic

41B93C9D-C5C3-46CB-AA4E-484B57EF5EDB

### Overview

Acquires and registers shooting conditions in My Settings. RICOH THETA V firmware v2.30.1 and later.

Conditions registered in My Settings are updated when the camera is turned on for RICOH THETA V.  
Conditions registered in My Settings are updated when switching to My Settings mode for RICOH THETA Z1 and later.

If [My Setting Capture Mode](my_setting_capture_mode.md) is video capture mode, mandatory value field must be set zero.

### Value Fields (RICOH THETA Z1 and later)

| Name | Type | Description |
|:--|:--|:--|
| [Shooting Method](../shooting_control_command_v2/shooting_method.md) | sint8 | Shooting Method<br>Set Normal shooting when [My Setting Capture Mode](my_setting_capture_mode.md) is set movie shooting mode |
| [File Format](file_format.md) | sint8 | Recording Size |
| [Exposure Program](exposure_program.md) | sint8 | Exposure Program |
| [Aperture](../shooting_control_command_v2/aperture.md) | sint8 | Aperture Value |
| [Shutter Speed](shutter_speed.md) | sint8 | Shutter Speed |
| [ISO](iso.md) | sint16 | ISO Sensitivity |
| [ISO Auto High Limit](../shooting_control_command_v2/iso_auto_high_limit.md) | sint16 | ISO Sensitivity Upper Limit |
| [Exposure Compensation](exposure_compensation.md) | sint8 | EV Compensation |
| [White Balance](white_balance.md) | sint8 | White Balance |
| [Color Temperature](color_temperature.md) | sint16 | Color Temperature |
| [Filter](filter.md) | sint8 | Image Processing Filter<br>Set OFF when [My Setting Capture Mode](my_setting_capture_mode.md) is set movie shooting mode |
| [Exposure Delay](exposure_delay.md) | sint8 | Self-timer Time |
| [White Balance Auto Strength](../shooting_control_command_v2/white_balance_auto_strength.md) | sint8 | To set the strength of white balance auto for low color temperature scene. |
| [Max Recordable Time](max_recordable_time.md) | sint8 | Maximum recordable time<br>Set if [My Setting Capture Mode](my_setting_capture_mode.md) is set movie shooting mode |

#### Add below with respect to Shooting Method

##### For interval shooting

| Name | Type | Description |
|:--|:--|:--|
| [Capture Number](capture_number.md) | sint16 | Number of Shots |
| [Capture Interval](capture_interval.md) | sint16 | Shooting Interval |

##### For interval composite shooting

| Name | Type | Description |
|:--|:--|:--|
| [Composite Shooting Time](../shooting_control_command_v2/composite_shooting_time.md) | sint32 | Shooting Time |
| [Composite Shooting Output Interval](../shooting_control_command_v2/composite_shooting_output_interval.md) | sint16 | In-progress Save Interval |

##### For multi bracket shooting

| Name | Type | Description |
|:--|:--|:--|
| Number of Bracket Shots | sint8 | Number of shots in multi bracketing.<br>2 to 13. |

Requests for data in the following format for the number of bracket shots.

| Name | Type | Description |
|:--|:--|:--|
| [Exposure Program](exposure_program.md) | sint8 | Exposure Program |
| [Aperture](../shooting_control_command_v2/aperture.md) | sint8 | Aperture Value |
| [Shutter Speed](shutter_speed.md) | sint8 | Shutter Speed |
| [ISO](iso.md) | sint16 | ISO Sensitivity |
| [Exposure Compensation](exposure_compensation.md) | sint8 | EV Compensation |
| [White Balance](white_balance.md) | sint8 | White Balance |
| [Color Temperature](color_temperature.md) | sint16 | Color Temperature |

##### For burst shooting

Requests for data in the following format for [BurstOption](../shooting_control_command_v2/burst_option.md).

| Name | Type | Description |
|:--|:--|:--|
| burstCaptureNum | sint8 | Number of shots for burst shooting |
| burstBracketStep | sint8 | Bracket value range between each shot for burst shooting |
| burstCompensation | sint8 | Exposure compensation for the base image and entire shooting for burst shooting |
| burstMaxExposureTime | sint8 | Maximum exposure time for burst shooting |
| burstEnableISOControl | sint8 | Adjustment with ISO sensitivity for burst shooting |
| burstOrder | sint8 | Shooting order for burst shooting |

### Value Fields (RICOH THETA V)

#### For RICOH THETA V firmware v3.00.1 and later

| Name | Type | Description |
|:--|:--|:--|
| [Shooting Method](../shooting_control_command_v2/shooting_method.md) | sint8 | Shooting Method<br>Set Normal shooting only. |
| [File Format](file_format.md)\* | sint8 | Recording Size<br>Set -1 for choise "Do not update My Setting condition." |
| [Exposure Program](exposure_program.md) | sint8 | Exposure Program |
| [Aperture](../shooting_control_command_v2/aperture.md) | sint8 | Aperture Value<br>Set AUTO only. |
| [Shutter Speed](shutter_speed.md) | sint8 | Shutter Speed |
| [ISO](iso.md) | sint16 | ISO Sensitivity |
| [ISO Auto High Limit](../shooting_control_command_v2/iso_auto_high_limit.md)\* | sint16 | ISO Sensitivity Upper Limit<br>Set -1 for choise "Do not update My Setting condition."<br>(RICOH THETA V firmware v3.03.1 and later) |
| [Exposure Compensation](exposure_compensation.md) | sint8 | EV Compensation |
| [White Balance](white_balance.md) | sint8 | White Balance |
| [Color Temperature](color_temperature.md) | sint16 | Color Temperature |
| [Filter](filter.md) | sint8 | Image Processing Filter<br>Set OFF when [My Setting Capture Mode](my_setting_capture_mode.md) is set movie shooting mode. |
| [Exposure Delay](exposure_delay.md)\* | sint8 | Self-timer Time<br>Can not set 0<br>Set -1 for choise "Do not update My Setting condition." |
| [Max Recordable Time](max_recordable_time.md)\* | sint8 | Maximum recordable time<br>Set if [My Setting Capture Mode](my_setting_capture_mode.md) is set movie shooting mode.<br>Set -1 for choise "Do not update My Setting condition." |

\* Persistence options. Can be set the choice "Do not update My Setting condition on power-on."<br>In that case, the camera will start up with the option values stored on turn-off even if another My Setting condition is registered.

#### RICOH THETA V firmware v2.50.1 and earlier

| Name | Type | Description |
|:--|:--|:--|
| [Exposure Program](exposure_program.md) | sint8 | Exposure Program |
| [Shutter Speed](shutter_speed.md) | sint8 | Shutter Speed |
| [ISO](iso.md) | sint16 | ISO Sensitivity |
| [Exposure Compensation](exposure_compensation.md) | sint8 | EV Compensation |
| [White Balance](white_balance.md) | sint8 | White Balance |
| [Color Temperature](color_temperature.md) | sint16 | Color Temperature |
| [Filter](filter.md) | sint8 | Image Processing Filter<br>Set OFF when [My Setting Capture Mode](my_setting_capture_mode.md) is set movie shooting mode |

### Properties

| Property | Requirement |
|:--|:--|
| Read | Mandatory |
| Write | Mandatory |
| Notify | Excluded |
