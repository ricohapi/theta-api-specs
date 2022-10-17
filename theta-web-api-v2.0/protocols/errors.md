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
| invalidSessionId | 403 | sessionID when command was issued is invalid |
| invalidParameterValue | 400 | Parameter value when command was issued is invalid |
| corruptedFile | 403 | Process request for corrupted file |
| cameraInExclusiveUse | 400 | Session start not possible when camera is in exclusive use |
| powerOffSequenceRunning | 403 | Process request when power supply is off |
| invalidFileFormat | 403 | Invalid file format specified |
| serviceUnavailable | 503 | Processing requests cannot be received temporarily |
 canceledShooting | 403 | Shooting request cancellation of the self-timer.<br>Returned in [Commands/Status](commands_status.md) of [camera.takePicture](../commands/camera.take_picture.md)<br>(RICOH THETA S firmware version 01.42 or later) |
| unexpected | 503 | Other errors |

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
