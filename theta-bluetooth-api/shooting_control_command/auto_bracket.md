# Auto Bracket

### Service

1D0F3602-8DFB-4340-9045-513040DAD991

### Characteristic

0387F5A3-26F5-4A67-B3C7-A78BBF17DFF7

### Overview

Acquires and sets the bracketing settings.

### Value Fields

| Name | Type | Description |
|:--|:--|:--|
| Number of Bracket Shots | sint8 | Number of shots in multi bracketing.<br>2 to 13 (RICOH THETA V firmware v2.50.1 or prior), 2 to19 (RICOH THETA Z1 and RICOH THETA V firmware v3.00.1 or later). |

Requests for data in the following format for the number of bracket shots.

#### For RICOH THETA Z1 and V firmware v3.00.1 or later

\<Exposure Program\>\<Aperture\>\<Shutter Speed\>\<ISO\>\<Exposure Compensation\>\<White Balance\>\<Color Temperature\>

#### For RICOH THETA V firmware v2.50.1 or prior

\<ISO\>\<Shutter Speed\>\<Color Temperature\>

| Name | Type | Note |
|:--|:--|:--|
| [ISO](iso.md) | sint16 | --- |
| [Shutter Speed](shutter_speed.md) | sint8 | --- |
| [Color Temperature](color_temperature.md) | sint16 | --- |
| [Exposure Program](exposure_program.md) | sint8 | --- |
| [Aperture](../shooting_control_command_v2/aperture.md) | sint8 | Set 0 for RICOH THETA V. |
| [Exposure Compensation](exposure_compensation.md) | sint8 | --- |
| [White Balance](white_balance.md) | sint8 | --- |

### Properties

| Property | Requirement |
|:--|:--|
| Read | Mandatory |
| Write | Mandatory |
| Notify | Excluded |
