# camera.delete

### Overview

Deletes still image or video files.  
 If "fileUrls" contains the file URL that does not exist or that cannot be deleted, an error occurs, and all specified files cannot be deleted.

### Parameters

| Name | Type | Description |
|:--|:--|:--|
| fileUrls | String Array | URLs of the file to delete<br>The number of file URLs is up to 128.<br>When you want to delete all at once, special parameters can be used: "all" as all files, "image" as all still images and "video" as all videos. (These should be specified alone.) |

### Results

None.

### Restriction

This command cannot be executed during video recording.
