# exposureDelay

### Overview

Operating time (sec.) of the self-timer.   
(RICOH THETA S firmware version 01.42 and later)

If exposureDelay is enabled, self-timer is used by shooting in still image capture mode.  
If exposureDelay is disabled, use [\_latestEnabledExposureDelayTime](_latest_enabled_exposure_delay_time.md) to get the operating time of the self-timer stored in the camera.

The current setting can be acquired by [camera.getOptions](../commands/camera.get_options.md), and it can be changed by [camera.setOptions](../commands/camera.set_options.md).

### Support value

Values that can be set differ depending on the shooting mode ([captureMode](capture_mode.md)).

| Shooting mode | Support value |
|:--|:--|
| image | 0 (Disabled),<br>1, 2, 3, 4, 5, 6, 7, 8, 9, 10 (Enabled) |
| \_video | 0 |
| \_liveStreaming | 0 |
