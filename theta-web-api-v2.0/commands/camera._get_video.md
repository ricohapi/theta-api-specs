# camera.\_getVideo

### Overview

Acquires video.

### Parameters

| Name | Type | Description |
|:--|:--|:--|
| fileUri | String | ID of the file to be acquired |
| type | String | Type of file to be acquired<br>Specify "thumb" or "full"<br>Set to "full" by default if unspecified<br>(thumb: Thumbnail image, full: Original size video) |

### Output

Binary data of the thumbnail image (JPEG) or video (MP4).

### Restriction

This command cannot be executed during video recording.
