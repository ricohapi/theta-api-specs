# camera.\_listAll

### Overview

Acquires a list of still image files and movie files.

### Parameters

| Name | Type | Description |
|:--|:--|:--|
| entryCount | Integer | Number of still image files and movie files to acquire. |
| continuationToken | String | (Optional)<br>A token to resume reading at the end of the previous \_listAll result. |
| detail | Boolean | (Optional)<br>Specifies whether or not to acquire the file details.<br>Default is "true" and file details are acquired.<br>If set to "false", "name", "uri", "size", and "dateTime" can only be acquired. |
| sort | String | (Optional)<br>Specifies the sort order.<br>Chose from "newest" (in the descending order of dateTime values) and "oldest" (in the ascending order of dateTime values).<br>Default is "newest". |

### Results

| Name | Type | Description |
|:--|:--|:--|
| entries | Object | The list of still image files and movie files acquired.<br>Refer to the next section for details. |
| totalEntries | Integer | Number of still image files and movie files stored in the camera. |
| continuationToken | String | A token to resume reading at the end of the file list acquired last time.<br>Omitted when the list contains the last file. |

### entries object

| Name | Type | Description |
|:--|:--|:--|
| name | String | File name |
| uri | String | File ID |
| size | Integer | File sizes (bytes) |
| dateTimeZone | String | File creation or update time with the time zone.<br>Can be acquired when "detail" is "true". |
| dateTime | String | File creation or update time.<br>Local time.<br>Can be acquired when "detail" is "false". |
| lat | Number | Latitude<br>Can be obtained for data shot with GPS enabled. |
| lng | Number | Longitude<br>Can be obtained for data shot with GPS enabled. |
| width | Integer | Horizontal size of image (pixels) |
| height | Integer | Vertical size of image (pixels) |
| \_intervalCaptureGroupId | String | Group ID of a still image shot by interval shooting.<br>Can be obtained if a still image was shot by interval shooting. |
| \_compositeShootingGroupId | String | Group ID of a still image shot by interval composite shooting.<br>Can be obtained if a still image was shot by interval composite shooting.<br>(RICOH THETA S firmware v01.82 or later and RICOH THETA SC firmware v1.10 or later) |
| \_autoBracketGroupId | String | Group ID of a still image shot by multi bracket shooting.<br>Can be obtained if a still image was shot by multi bracket shooting.<br>(RICOH THETA S firmware v01.82 or later and RICOH THETA SC firmware v1.10 or later) |
| recordTime | Integer | Video shooting time (sec)<br>Can be obtained for a movie file. |

### Restriction

Cannot be run while shooting a movie.

### Example

#### Parameters

```
{
    "entryCount": 3
}
```

#### Results

```
{
    "entries": [
        {
            "name": "R0010017.MP4",
            "uri": "100RICOH/R0010017.MP4",
            "size": 5135574,
            "dateTimeZone": "2015:07:10 11:05:18+09:00",
            "width": 1920,
            "height": 1080,
            "recordTime": 2
        },
        {
            "name": "R0010016.JPG",
            "uri": "100RICOH/R0010016.JPG",
            "size": 4214389,
            "dateTimeZone": "2015:07:10 11:00:35+09:00",
            "width": 5376,
            "height": 2688
        },
        {
            "name": "R0010015.JPG",
            "uri": "100RICOH/R0010015.JPG",
            "size": 4217265,
            "dateTimeZone": "2015:07:10 11:00:34+09:00",
            "width": 5376,
            "height": 2688
        }
    ],
    "totalEntries": 16,
    "continuationToken": "12"
}
```

### Example (when "detail" is "false")

#### Parameters

```
{
    "entryCount": 3,
    "detail": false
}
```

#### Results

```
{
    "entries": [
        {
            "name": "R0010034.JPG",
            "uri": "100RICOH/R0010034.JPG",
            "size": 4134436,
            "dateTime": "2015:07:17 14:13:14"
        },
        {
            "name": "R0010033.JPG",
            "uri": "100RICOH/R0010033.JPG",
            "size": 4167440,
            "dateTime": "2015:07:16 14:15:22"
        },
        {
            "name": "R0010032.JPG",
            "uri": "100RICOH/R0010032.JPG",
            "size": 4138995,
            "dateTime": "2015:07:16 14:15:00"
        }
    ],
    "totalEntries": 34,
    "continuationToken": "30"
}
```
