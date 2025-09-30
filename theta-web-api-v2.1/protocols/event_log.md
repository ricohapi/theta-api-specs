# EventLog

### API

GET `/log/eventLog`

### Overview

Acquires latest logs.

### Support model

| X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|
| v2.80.1 and later | v3.50.2 and later | --- | --- | --- |

### Request

None.

### Response

* Content-Type: text/plain; charset=utf-8  
* Response body: Latest logs.  

Sample

```
[2025/07/01 11:30:00] [Button] Power On
[2025/07/01 11:30:15] [NTP] set 2025:07:01 11:30:20
[2025/07/01 11:30:30] [USB] MTP connected
[2025/07/01 11:30:45] [USB] MTP disconnected
[2025/07/01 12:00:00] [Button] [Image] takePicture
[2025/07/01 12:00:05] [SaveFile] 100RICOH/R0010001.JPG
[2025/07/01 12:00:10] [Button] [Video] startCapture
[2025/07/01 12:00:20] [Button] [Video] stopCapture
[2025/07/01 12:00:22] [SaveFile] 100RICOH/R0010002.MP4
```
