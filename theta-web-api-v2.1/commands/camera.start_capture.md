# camera.startCapture

### Overview

Starts continuously shoots.   
The shooting method changes according to the shooting mode ([captureMode](../options/capture_mode.md)) and \_mode settings.

In the still image shooting mode, interval shooting, interval composite shooting, multi bracket shooting, time shift shooting, burst shooting and continuous shooting is started depending on the \_mode setting.   
In the movie shooting mode, movie shooting is started.

If [exposureDelay](../options/exposure_delay.md) is enabled, self-timer shooting is started. Time shift shooting ignores self-timer.

For movie shooting or interval shooting with no shot count specified, "state" for [Commands/Execute](../protocols/commands_execute.md#output) and [Commands/Status](../protocols/commands_status.md) changes to "done" immediately.  
 For interval shooting with the shot count specified, interval composite shooting, multi bracket shooting, time shift shooting, or continuous shooting, progress information can be acquired from the progress object of [Commands/Execute](../protocols/commands_execute.md#output) and [Commands/Status](../protocols/commands_status.md). Also, "state" changes to "done" when shooting of the specified number of shots or shooting of the specified period of time has been finished.  

 For RICOH THETA X, it is necessary to switch the shooting method using [_shootingMethod](../options/_shooting_method.md) before executing this API.  

### Support model

| Shooting mode | X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|:--|
| Interval shooting | All | All | All | All | v01.62 or later |
| Multi bracket shooting | All | All | All | v1.10 or later | v01.82 or later |
| Interval composite shooting | --- | All | --- | v1.10 or later | v01.82 or later |
| Time shift shooting | All | All | v3.00.1 or later | --- | --- |
| Movie shooting | All | All | All | All | v01.62 or later |
| Interval shooting (optimized <span class="mintext">*1</span>, Tripod stabilization Off) | --- | v1.50.1 or later | v3.40.1 or later | --- | --- |
| Interval shooting (optimized <span class="mintext">*1</span>, Tripod stabilization On) | --- | v1.50.1 or later | v3.40.1 or later | --- | --- |
| Burst shooting | --- | v2.10.1 or later | --- | --- | --- |
| Continuous shooting | All | --- | --- | --- | --- |

\*1 Top/bottom correction and stitching conditions are optimized.

### Parameters

| Name | Type | Description |
|:--|:--|:--|
| \_mode | String | Continuously shoots in the still image shooting mode.<br>Interval shooting is started if this parameter is omitted<br>(interval: Interval shooting, composite: Interval composite shooting, bracket: Multi bracket shooting, timeShift: Time shift shooting, burst: Burst shooting, continuous: Continuous shooting).<br>This parameter cannot be specified in the movie shooting mode. |

### Results

"Results" value when "state" of [Commands/Execute](../protocols/commands_execute.md#output) and [Commands/Status](../protocols/commands_status.md) is "done".  
 Depends on the shooting method.

#### For movie shooting or interval shooting with no shot count specified

None.

#### For interval shooting with the shot count specified, interval composite shooting, multi bracket shooting, time shift shooting, burst shooting or continuous shooting.

| Name | Type | Description |
|:--|:--|:--|
| fileUrls | String Array | List of file URLs |

### Restriction

Some commands cannot be run while shooting a movie.
