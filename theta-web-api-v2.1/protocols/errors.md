# Errors

### Overview

If an error occurs when API is called, an error object is included in the response.

Error information from the camera can be acquired by [State](state.md).

### Error object

| Error code | HTTP<br>Status code | Description |
|:--|:--|:--|
| unknownCommand | 400 | Invalid command is issued |
| disabledCommand | 403 | Command cannot be executed due to the camera status |
| missingParameter | 400 | Insufficient required parameters to issue the command |
| invalidParameterName | 400 | Parameter name or option name is invalid |
| invalidParameterValue | 400 | Parameter value when command was issued is invalid |
| tooManyParameters | 403 | Number of parameters exceeds limit |
| corruptedFile | 403 | Process request for corrupted file |
| powerOffSequenceRunning | 403 | Process request when power supply is off |
| invalidFileFormat | 403 | Invalid file format specified |
| serviceUnavailable | 503 | Processing requests cannot be received temporarily.<br>*Please try again after a modest amount of time |
| canceledShooting | 403 | Shooting request cancellation of the self-timer.<br>Returned in [Commands/Status](commands_status.md) of [camera.takePicture](../commands/camera.take_picture.md) or [camera.startCapture](../commands/camera.start_capture.md) |
| canceledConversion | 403 | Converting movie format request cancellation.<br>Returned in [Commands/Status](commands_status.md) of [camera.\_convertVideoFormats](../commands/camera._convert_video_formats.md) |
| unexpected | 503 | Other errors |
| notFound | 404 | There is no server or no page corresponding to the address |

### Example

```
{
    "state": "error",
    "error": {
        "code": "unknownCommand",
        "message": "Command executed is unknown."
    }
}
```
