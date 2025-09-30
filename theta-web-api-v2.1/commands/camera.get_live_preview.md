# camera.getLivePreview

### Overview

Acquires a live view.   
Only available in the still image shooting mode for RICOH THETA S and RICOH THETA SC.   
Available in the still image and movie shooting modes for RICOH THETA V and later.  
 Data acquisition stops when the camera is operated, shooting is started, or the shooting mode is changed.

### Parameters

None.

### Output

Binary data of live view (MotionJPEG).   
Binary data is transferred as Content-Type: multipart/x-mixed-replace.   
Refer to [here](../../ricoh-theta-api/README.md) for the image format.
