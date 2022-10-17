# camera.getImage

### Overview

Acquires images.

### Parameters

| Name | Type | Description |
|:--|:--|:--|
| fileUri | String | ID of the file to be acquired |
| \_type | String | Type of file to be acquired<br>Specify "thumb" or "full"<br>Set to "full" by default if unspecified<br>(thumb: Thumbnail image, full: Original size image) |

### Output

Binary data for image (JPEG).

### Restriction

This command cannot be executed during video recording.
