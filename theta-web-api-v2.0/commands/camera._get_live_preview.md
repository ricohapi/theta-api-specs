# camera.\_getLivePreview

### Overview

Acquires the Live View. Can only be executed in still image capture mode.   
 Data acquisition is finished when the camera is operated, shooting starts or the shooting mode is switched.

### Parameters

| Name | Type | Description |
|:--|:--|:--|
| sessionId | String | Session ID<br>Specify the value acquired by [camera.startSession](camera.start_session.md) |

### Output

Binary data (MotionJPEG) for Live View.   
 Binary data is transferred by Content-Type: multipart/x-mixed-replace.  
See [Introduction](../../theta-api-introduction/README.md) for details on the image format.
