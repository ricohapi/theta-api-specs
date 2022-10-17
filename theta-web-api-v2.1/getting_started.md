# Getting Started

RICOH THETA S and later models send and receive data over HTTP connection, dissimilarly to RICOH THETA and RICOH THETA m15.

This section explains the following flow from shooting a still image through acquiring the stored file.

1. [Specify the API version](#1-specify-the-api-version)
1. [Acquire status before shooting](#2-acquire-status-before-shooting)
1. [Acquire and set properties](#3-acquire-and-set-properties)
1. [Shoot a still image](#4-shoot-a-still-image)
1. [Check for file saving](#5-check-for-file-saving)
1. [Acquire the file](#6-acquire-the-file)

### 1. Specify the API version

For RICOH THETA V or later, start from "2. Acquire status before shooting" since its API version is set to RICOH THETA API v2.1 by default.

For RICOH THETA S and RICOH THETA SC, since the API version is set to RICOH THETA API v2.0 when connection is established via wireless LAN, you need to use [clientVersion](../theta-web-api-v2.0/options/client_version.md) to set the API version of the camera to v2.1.

API v2.0 requires a session to start before running command. Use [camera.startSession](../theta-web-api-v2.0/commands/camera.start_session.md) to start a session and [camera.setOptions](../theta-web-api-v2.0/commands/camera.set_options.md) to set the camera and shooting properties.

#### Request (to start a session)

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

#### Request (to specify the API version)

```
POST /osc/commands/execute
{
    "name": "camera.setOptions",
    "parameters": {
        "sessionId": "SID_0001",
        "options": {
            "clientVersion": 2
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

### 2. Acquire status before shooting

Acquire the status of the camera in preparation for determining if the file has been saved.

Use [State](protocols/state.md) to check the state ID (fingerprint) and the latest file URL (state.\_latestFileUrl).

#### Request

```
POST /osc/state
```

#### Response

```
{
    "fingerprint": "FIG_0003",
    "state": {
        "batteryLevel": 1.0,
        "storageUri": "http://192.168.1.1/files/abcde/",
        "_captureStatus": "idle",
        "_recordedTime": 0,
        "_recordableTime": 0,
        "_latestFileUrl": "http://192.168.1.1/files/abcde/100RICOH/R0010004.MP4",
        "_batteryState": "disconnect",
        "_apiVersion": 2
    }     
}
```

### 3. Acquire and set properties

Use [camera.getOptions](commands/camera.get_options.md) to acquire the camera and shooting properties.

The following shows an example of acquiring the image format ([fileFormat](options/file_format.md)) and its supported values.

\* The following sample applies to RICOH THETA S and RICOH THETA SC.

#### Request

```
POST /osc/commands/execute
{
    "name": "camera.getOptions",
    "parameters": {
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

Use [camera.setOptions](commands/camera.set_options.md) to set the camera and shooting properties.

The following shows an example of setting the image format ([fileFormat](options/file_format.md)) to set the still image size to 2048 x 1024 pixels.

#### Request

```
POST /osc/commands/execute
{
    "name": "camera.setOptions",
    "parameters": {
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

### 4. Shoot a still image

Press the shutter release button. The command used depends on whether still images are shot by single shooting or continuous shooting.

[camera.takePicture](commands/camera.take_picture.md) is used to shoot a single still image, and [camera.startCapture](commands/camera.start_capture.md) and [camera.stopCapture](commands/camera.stop_capture.md) are used to shoot images continuously.

#### Request

```
POST /osc/commands/execute
{
    "name": "camera.takePicture"
}
```

#### Response

For shooting a still image, "state" immediately after pressing the shutter release button is returned as "inProgress."

```
{
    "name": "camera.takePicture",
    "state": "inProgress",
    "id": "1",
    "progress": {
        "completion": 0.00
    }
}
```

### 5. Check for file saving

Use [CheckForUpdates](protocols/check_for_updates.md) to check for update of the camera status and [State](protocols/state.md) to detect completion of file saving.

#### Request

Change of the camera status can be checked with change of the status ID (stateFingerprint) of [CheckForUpdates](protocols/check_for_updates.md).

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

When the file has been saved, URL of the saved file is stored in "state.\_latestFileUrl" of [State](protocols/state.md). If the status changes to other than file saving completion or does not change until [CheckForUpdates](protocols/check_for_updates.md) times out, call this API repeatedly until the status changes to file saving completion.

```
POST /osc/state
```

#### Response

```
{
    "fingerprint": "FIG_0006",
    "state": {
        "batteryLevel": 0.67,
        "storageUri": "http://192.168.1.1/files/abcde/",
        "_captureStatus": "idle",
        "_recordedTime": 0,
        "_recordableTime": 0,
        "_latestFileUrl": "http://192.168.1.1/files/abcde/100RICOH/R0010005.JPG",
        "_batteryState": "disconnect", "_apiVersion": 2
    }
}
```

### 6. Acquire the file

Use the file URL and the GET request to acquire the file.

To correct the zenith of the acquired still image, use XMP (GPano:PosePitchDegrees / GPano:PoseRollDegrees) contained in the image data. Refer to [Photo Sphere XMP Metadata](https://developers.google.com/streetview/spherical-metadata/) for the details of XMP.

#### Request

```
GET /files/abcde/100RICOH/R0010005.JPG
```

#### Response

```
(Binary data)
```
