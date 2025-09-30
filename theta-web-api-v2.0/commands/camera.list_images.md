# camera.listImages

### Overview

Acquires the still image file list.

### Parameters

| Name | Type | Description |
|:--|:--|:--|
| entryCount | Integer | No. of still image files to be acquired |
| maxSize | Integer | Fixed value<br>for maximum size of thumbnails: 160<br>Required parameter when includeThumb is true |
| continuationToken | String | (Optional)<br>Token for reading the continuation from the previous listImages. |
| includeThumb | Boolean | (Optional)<br>Whether thumbnails are required<br>Default is true and thumbnails are acquired<br>When includeThumb is true, you can get only one file. If you want to get a file list, it is recommended that you set includeThumb to false |

### Results

| Name | Type | Description |
|:--|:--|:--|
| entries | Object | File list of acquired still image files<br>Details in the following item |
| totalEntries | Integer | No. of still image files in the camera |
| continuationToken | String | Token for acquiring the file list continuation<br>Omitted if the last file is included in the list |

### entries object

| Name | Type | Description |
|:--|:--|:--|
| name | String | File name |
| uri | String | File ID |
| size | Integer | File size (byte) |
| dateTimeZone | String | Time that a file with a time zone is created or updated |
| lat | Number | Latitude<br>Can be acquired for an image shot when GPS is enabled |
| lng | Number | Longitude<br>Can be acquired for an image shot when GPS is enabled |
| width | Integer | Width of the image (px) |
| height | Integer | Height of the image (px) |
| thumbnail | String | Thumbnail<br>Encoded in base64<br>Can be acquired when includeThumb is true |
| \_thumbSize | Integer | Thumbnail file size (byte)<br>Can be acquired when includeThumb is true |
| \_intervalCaptureGroupId | String | Group ID of still images shot using interval shooting<br>Can be acquired when images are shot using interval shooting |
| \_compositeShootingGroupId | String | Group ID of still images shot using interval composite shooting<br>Can be acquired when images are shot using interval composite shooting<br>(RICOH THETA S only; firmware version 01.82 and later) |
| \_autoBracketGroupId | String | Group ID of still images shot using multi bracket shooting<br>Can be acquired when images are shot using multi bracket shooting<br>(RICOH THETA S only; firmware version and later) |

### Restriction

This command cannot be executed during video recording.

### Example (when includeThumb is false)

#### Parameters

```
{
    "entryCount": 3,
    "includeThumb": false
}
```

#### Results

```
{
    "entries": [
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
        },
        {
            "name": "R0010014.JPG",
            "uri": "100RICOH/R0010014.JPG",
            "size": 4052147,
            "dateTimeZone": "2015:07:10 11:00:13+09:00",
            "width": 5376,
            "height": 2688
        }
    ],
    "totalEntries": 16,
    "continuationToken": "12"
}
```

### Example (when includeThumb is true)

#### Parameters

```
{
    "entryCount": 3,
    "maxSize": 160,
    "includeThumb": true
}
```

#### Results

```
{
    "entries": [
        {
            "name": "R0010016.JPG",
            "uri": "100RICOH/R0010016.JPG",
            "size": 4214389,
            "dateTimeZone": "2015:07:10 11:00:35+09:00",
            "width": 5376,
            "height": 2688,
            "thumbnail": "(base64_binary)",
            "_thumbSize": 3136
        }
    ],
    "totalEntries": 16,
    "continuationToken": "14"
}
```
