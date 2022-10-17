# camera.takePicture

### Overview

Starts still image shooting.

If [exposureDelay](../options/exposure_delay.md) is enabled, self-timer shooting is started.

### Parameters

None.

### Results

The results value when state of [Commands/Execute](../protocols/commands_execute.md#output) and [Commands/Status](../protocols/commands_status.md) are "done"

| Name | Type | Description |
|:--|:--|:--|
| fileUrl | String | URL of the captured still image file |
| \_dngFileUrl | String | DNG file URL when shooting with raw+<br>(RICOH THETA Z1 or later) |
