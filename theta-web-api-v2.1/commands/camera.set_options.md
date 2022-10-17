# camera.setOptions

### Overview

Property settings for shooting, the camera, etc.

Check the properties that can be set and specifications by the API v2.1 reference options category or [camera.getOptions](camera.get_options.md).

There is a detailed example of the request in [Getting Started.](../getting_started.md#3-acquire-and-set-properties)  

Leave an interval of 1 second or more between changing the settings in [camera.setOptions](camera.set_options.md) and executing [camera.getLivePreview](camera.get_live_preview.md), [camera.takePicture](camera.take_picture.md), or [camera.startCapture](camera.start_capture.md).  
Leave an interval of 1 second or more between changing the [_filter](../options/_filter.md) setting and changing the [captureMode](../options/capture_mode.md) setting. 

### Parameters

| Name | Type | Description |
|:--|:--|:--|
| options | Object | Set of option names and setting values to be set in JSON format |

### Results

None

### Example

#### Parameters

```
{
    "options": {
        "iso": 200
    }
}
```
