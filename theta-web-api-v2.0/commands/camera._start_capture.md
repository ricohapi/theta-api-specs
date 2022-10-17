# camera.\_startCapture

### Overview

Starts continuous shooting.   
The shooting method changes according to the shooting mode ([captureMode](../options/capture_mode.md)) and mode settings.   
The interval composite shooting and multi bracket shooting are supported by RICOH THETA S (firmware 01.82 or later) and RICOH THETA SC (firmware v1.10 or later) only.

In the still image shooting mode, interval shooting, interval composite shooting, or multi bracket shooting is started depending on the mode setting. If [exposureDelay](../options/exposure_delay.md) is enabled, self-timer shooting is started.   
In the movie shooting mode, movie shooting is started.

### Parameters

| Name | Type | Description |
|:--|:--|:--|
| sessionId | String | Session ID<br>Specify the value acquired by [camera.startSession](camera.start_session.md). |
| mode | String | Continuous shooting method in the still image shooting mode<br>Interval shooting is started if this parameter is omitted<br>(interval: Interval shooting, composite: Interval composite shooting: bracket: multi bracket shooting).<br>This parameter cannot be specified in the movie shooting mode. |

### Results

None.

### Restriction

Some commands cannot be run while shooting a movie.
