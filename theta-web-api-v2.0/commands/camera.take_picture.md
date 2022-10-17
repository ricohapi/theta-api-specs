# camera.takePicture

### Overview

Starts still image shooting.

If [exposureDelay](../options/exposure_delay.md) is enabled, self-timer shooting is started.

### Parameters

| Name | Type | Description |
|:--|:--|:--|
| sessionId | String | Session ID<br>Specify the value acquired by [camera.startSession](camera.start_session.md) |

### Results

The results value when state of [Commands/Execute](../protocols/commands_execute.md#output) and [Commands/Status](../protocols/commands_status.md) are "done"

| Name | Type | Description |
|:--|:--|:--|
| fileUri | String | ID of the captured still image file |
