# camera.listFiles

### Overview

Acquires a list of still image files and movie files.

### Parameters

| Name | Type | Description |
|:--|:--|:--|
| fileType | String | File types to acquire.<br>(all: All types, image: Still image, video: Movie) |
| startPosition | Integer | (Optional)<br>Position to start acquiring the file list.<br>If a number larger than the number of existing files is specified, a null list is acquired.<br>Default is the top of the list. |
| \_startFileUrl | String | (Optional)<br>First file to return to the list.<br>The list is acquired starting from the specified file position.<br>(RICOH THETA V or later) |
| entryCount | Integer | Number of still image and movie files to acquire.<br>If the number of existing files is smaller than the specified number of files, all available files are only acquired.<br>Note that a thumbnail can be acquired for a single file only. |
| maxThumbSize | Integer | Thumbnail.<br>(640: Acquire thumbnail, 0: Do not acquire thumbnail)<br>Be sure to specify this parameter regardless of the value of \_detail. |
| \_detail | Boolean | (Optional)<br>Specifies whether or not to acquire the file details.<br>Default is "true".<br>If set to "false", "name", "fileUrl", "size", "dateTime", "isProcessed", "previewUrl", and "\_favorite" can only be acquired. |
| \_sort | String | (Optional)<br>Specifies the sort order.<br>Choose from "newest" (in the descending order of the shooting date/time) and "oldest" (in the ascending order of the shooting date/time).<br>Default is "newest". |
| \_storage | String | (Optional)<br>Specifies the srorage.<br>"IN" : internal storage<br>"SD" : external storage (SD card)<br>"Default" : current storage<br>Default is "Default".<br>(RICOH THETA X Version 2.00.0 or later) |

### Results

| Name | Type | Description |
|:--|:--|:--|
| entries | Object | The list of still image files and movie files acquired.<br>Refer to the next section for details. |
| totalEntries | Integer | Number of still image files and movie files stored in the camera. |

### entries object

| Name | Type | Description |
|:--|:--|:--|
| name | String | File name. |
| fileUrl | String | File URL. |
| size | Integer | File sizes (bytes). |
| dateTimeZone | String | File creation or update time with the time zone.<br>Can be acquired when "\_detail" is "true". |
| dateTime | String | File creation or update time.<br>Local time.<br>Can be acquired when "\_detail" is "false". |
| lat | Number | Latitude.<br>Can be obtained for data shot with GPS enabled.<br>Can be acquired when "\_detail" is "true". |
| lng | Number | Longitude.<br>Can be obtained for data shot with GPS enabled.<br>Can be acquired when "\_detail" is "true". |
| width | Integer | Horizontal size of image (pixels).<br>Can be acquired when "\_detail" is "true". |
| height | Integer | Vertical size of image (pixels).<br>Can be acquired when "\_detail" is "true". |
| thumbnail | String | Thumbnail.<br>Can be acquired if Base64-<br>encoded maxThumbSize is enabled.<br>Can be acquired when "\_detail" is "true". |
| \_thumbSize | Integer | Thumbnail file size (bytes).<br>Can be acquired if maxThumbSize is enabled.<br>Can be acquired when "\_detail" is "true". |
| \_intervalCaptureGroupId | String | Group ID of a still image shot by interval shooting.<br>Can be obtained if a still image was shot by interval shooting.<br>Can be acquired when "\_detail" is "true". |
| \_compositeShootingGroupId | String | Group ID of a still image shot by interval composite shooting.<br>Can be obtained if a still image was shot by interval composite shooting.<br>Can be acquired when "\_detail" is "true".<br>(RICOH THETA Z1, RICOH THETA S firmware v01.82 or later and RICOH THETA SC firmware v1.10 or later) |
| \_autoBracketGroupId | String | Group ID of a still image shot by multi bracket shooting.<br>Can be obtained if a still image was shot by multi bracket shooting.<br>Can be acquired when "\_detail" is "true".<br>(RICOH THETA X, RICOH THETA Z1, RICOH THETA V, RICOH THETA S firmware v01.82 or later and RICOH THETA SC firmware v1.10 or later) |
| \_recordTime | Integer | Video shooting time (sec).<br>Can be obtained for a movie file.<br>Can be acquired when "\_detail" is "true". |
| isProcessed | Boolean | Whether or not image processing has been completed. |
| previewUrl | String | URL of the file being processed. |
| \_codec | String | Codec.<br>"H.264/MPEG-4 AVC"<br>Can be acquired when "\_detail" is "true".<br>(RICOH THETA V or later) |
| \_projectionType | String | Projection type of movie file.<br>"Equirectangular", "Dual-Fisheye" or "Fisheye".<br>Can be acquired when "\_detail" is "true".<br>(RICOH THETA V or later) |
| \_continuousShootingGroupId | String | continuousShootingGroupId.<br>Can be acquired when "\_detail" is "true".<br>(RICOH THETA X or later) |
| \_frameRate | Integer | Frame rate.<br>Can be acquired when "\_detail" is "true".<br>(RICOH THETA Z1 Version 3.01.1 or later, RICOH THETA X or later) |
| \_favorite | Boolean | Favorite.<br>(RICOH THETA X or later) |
| \_imageDescription | String | Image description.<br>Can be acquired when "\_detail" is "true".<br>(RICOH THETA X or later) |
| \_storageID | String | Storage ID.<br />Can be acquired when "\_detail" is "true".<br>(RICOH THETA X Version 2.00.0 or later) |

### Restriction

Cannot be run while shooting a movie.

### Example (RICOH THETA V)

#### Parameters

```
{
    "fileType": "all",
    "entryCount": 3,
    "maxThumbSize": 640
}
```

#### Results

```
{
    "entries": [
        {
            "name": "R0010017.JPG",
            "fileUrl": "http://192.168.1.1/files/abcde/100RICOH/R0010017.JPG",
            "size": 4051440,
            "dateTimeZone": "2015:07:10 11:05:18+09:00",
            "lat": 50.5324,
            "lng": -120.2332,
            "width": 5376,
            "height": 2688,
            "isProcessed": true,
            "previewUrl": "",
            "thumbnail": "(base64_binary)",
            "_thumbSize": 3348,
        }
    ],
    "totalEntries": 16
}
```

### Example (when "\_detail" is "true" and thumbnail is not acquired)

#### Parameters

```
{
    "fileType": "all",
    "entryCount": 3,
    "maxThumbSize": 0
}
```

#### Results

```
{
    "entries": [
        {
            "name": "R0011607.JPG",
            "fileUrl": "http://192.168.1.1/files/abcde/100RICOH/R0011607.JPG",
            "size": 4051440,
            "dateTimeZone": "2016:06:29 17:06:58+09:00",
            "width": 5376,
            "height": 2688,
            "isProcessed": true,
            "previewUrl": ""
        },
        {
            "name": "R0011606.JPG",
            "fileUrl": "http://192.168.1.1/files/abcde/100RICOH/R0011606.JPG",
            "size": 4065630,
            "dateTimeZone": "2016:06:29 16:58:47+09:00",
            "width": 5376,
            "height": 2688,
            "isProcessed": true,
            "previewUrl": ""
        },
        {
            "name": "R0011605.JPG",
            "fileUrl": "http://192.168.1.1/files/abcde/100RICOH/R0011605.JPG",
            "size": 4057882,
            "dateTimeZone": "2016:06:29 16:55:26+09:00",
            "width": 5376,
            "height": 2688,
            "isProcessed": true,
            "previewUrl": ""
        }
    ],
    "totalEntries": 30
}
```

### Example (when "\_detail" is "false")

#### Parameters

```
{
    "fileType": "all",
    "entryCount": 3,
    "maxThumbSize": 640,
    "_detail": false
}
```

#### Results

```
{
    "entries": [
        {
            "name": "R0010034.JPG",
            "fileUrl": "http://192.168.1.1/files/abcde/100RICOH/R0010034.JPG",
            "size": 4134436,
            "dateTime": "2015:07:17 14:13:14",
            "isProcessed": true,
            "previewUrl": ""
        },
        {
            "name": "R0010033.JPG",
            "fileUrl": "http://192.168.1.1/files/abcde/100RICOH/R0010033.JPG",
            "size": 4167440,
            "dateTime": "2015:07:16 14:15:22",
            "isProcessed": true,
            "previewUrl": ""
        },
        {
            "name": "R0010032.JPG",
            "fileUrl": "http://192.168.1.1/files/abcde/100RICOH/R0010032.JPG",
            "size": 4138995,
            "dateTime": "2015:07:16 14:15:00",
            "isProcessed": true,
            "previewUrl": ""
        }
    ],
    "totalEntries": 34
}
```
