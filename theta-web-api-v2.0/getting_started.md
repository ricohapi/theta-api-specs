# Getting Started

Unlike the RICOH THETA and RICOH THETA m15, communication for the RICOH THETA S or above are performed via HTTP connection.

This section explains the flow from capturing a still image to acquiring the file.

1. [Start session](#1-start-session)
1. [Acquire status prior to shooting](#2-acquire-status-prior-to-shooting)
1. [Acquire/Set properties](#3-acquireset-properties)
1. [Shoot still image](#4-shoot-still-image)
1. [Confirm file save](#5-confirm-file-save)
1. [Acquire file](#6-acquire-file)
1. [End session](#7-end-session)

### 1. Start session

Session starts because it is required for shooting.

#### Request

```
POST /osc/commands/execute
{
    "name": "camera.startSession",
    "parameters": {}
}
```

#### Response

```
{
    "name": "camera.startSession",
    "state": "done",
    "results": {
        "sessionId": "SID_0001",
        "timeout": 180
    }
}
```

### 2. Acquire status prior to shooting

The status of the device is acquired as pre-preparation to confirm whether the file save process is complete.

Check the status ID (fingerprint) and newest file ID (state.\_latestFileUri) with [State](protocols/state.md).

#### Request

    POST /osc/state

#### Response

```
{
    "fingerprint": "FIG_0003",
    "state": {
        "sessionId": "SID_0001",
        "batteryLevel": 1.0,
        "storageChanged": false,
        "_captureStatus": "idle",
        "_recordedTime": 0,
        "_recordableTime": 0,
        "_latestFileUri": "100RICOH/R0010004.MP4",
        "_batteryState": "disconnect"
    }
}
```

### 3. Acquire/Set properties

In order to aquire specified properties, [camera.getOptions](commands/camera.get_options.md) is used.

This is an example of acquisition the image format property ([fileFormat](options/file_format.md)) and its support value.

#### Request

```
POST /osc/commands/execute
{
    "name": "camera.getOptions",
    "parameters": {
        "sessionId": "SID_0001",
        "optionNames": [
            "fileFormat",
            "fileFormatSupport"
        ]
    }
}
```

#### Response

```
{
    "name": "camera.getOptions",
    "state": "done",
    "results": {
        "options": {
            "fileFormat": {
                "type": "jpeg",
                "width": 5376,
                "height": 2688
            },
            "fileFormatSupport": [
                { "type": "jpeg", "width": 5376, "height": 2688 },
                { "type": "jpeg", "width": 2048, "height": 1024 }
            ]
        }
    }
}
```

In order to set specified properties, [camera.setOptions](commands/camera.set_options.md) is used.

This is an example of setting the image format property ([fileFormat](options/file_format.md)) for setting the still image size to 2048x1024.

#### Request

```
POST /osc/commands/execute
{
    "name": "camera.setOptions",
    "parameters": {
        "sessionId": "SID_0001",
        "options": {
            "fileFormat": {
                "type": "jpeg",
                "width": 2048,
                "height": 1024
            }
        }
    }
}
```

#### Response

```
{
    "name": "camera.setOptions",
    "state": "done"
}
```

### 4. Shoot still image

Operates the shutter. The shutter operation command differs depending on whether it is still image shooting, interval shooting or video shooting.

[camera.takePicture](commands/camera.take_picture.md) is used for still image shooting, and [camera.\_startCapture](commands/camera._start_capture.md) and [camera.\_stopCapture](commands/camera._stop_capture.md) are used for interval shooting and video shooting.

#### Request

```
POST /osc/commands/execute
{
    "name": "camera.takePicture",
    "parameters": {
        "sessionId": "SID_0001"
    }
}
```

#### Response

The state returns to "inProgress" immediately after the shutter is operated.

```
{
    "name": "camera.takePicture",
    "state": "inProgress",
    "id": "1",
    "progress": {
        "completion": 0
    }
}
```

### 5. Confirm file save

Check changes to the device status in [CheckForUpdates](protocols/check_for_updates.md), and detect whether file save is completed in [State](protocols/state.md).

#### Request

Changes to the device status can be checked by changes to the status ID (stateFingerprint) of [CheckForUpdates](protocols/check_for_updates.md).

```
POST /osc/checkForUpdates
{
    "stateFingerprint": "FIG_0003"
}
```

#### Response

```
{
    "stateFingerprint": "FIG_0004"
}
```

#### Request

When a file is saved, the file ID saved in state.\_latestFileUri of [State](protocols/state.md) is entered. If a status change other than file save occurs or the state does not change due to a [CheckForUpdates](protocols/check_for_updates.md) timeout, it is necessary to repeatedly call and wait until the file is saved.

```
POST /osc/state
```

#### Response

```
{
    "fingerprint": "FIG_0006",
    "state": {
        "sessionId": "SID_0001",
        "batteryLevel": 0.67,
        "storageChanged": false,
        "_captureStatus": "idle",
        "_recordedTime": 0,
        "_recordableTime": 0,
        "_latestFileUri": "100RICOH/R0010005.JPG",
        "_batteryState": "disconnect"
    }
}
```

### 6. Acquire file

Acquire the file. Use [camera.getImage](commands/camera.get_image.md) for still images and [camera.\_getVideo](commands/camera._get_video.md) for videos.

When performing the acquired still image top/bottom correction, use the XMP (GPano:PosePitchDegrees / GPano:PoseRollDegrees) contained in the image data. See [Photo Sphere XMP Metadata](https://developers.google.com/streetview/spherical-metadata/) for details on XMP.

#### Request

```
POST /osc/commands/execute
{
    "name": "camera.getImage",
    "parameters": {
        "fileUri": "100RICOH/R0010005.JPG"
    }
}
```

#### Response

```
(Binary data)
```

### 7. End session

Close the session.

#### Request

```
POST /osc/commands/execute
{
    "name": "camera.closeSession",
    "parameters": {
        "sessionId": "SID_0001"
    }
}
```
