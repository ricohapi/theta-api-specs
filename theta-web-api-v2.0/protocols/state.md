# State

### API

POST /osc/state

### Overview

Acquires the camera status.

Changes in the state object content can be checked with [CheckForUpdates](check_for_updates.md).

### Input

None.

### Output

| Name | Type | Description |
|:--|:--|:--|
| fingerprint | String | Current status ID<br>Obtain a unique value for each status |
| state | Object | Camera status (Details in the following item) |

### state object

Camera status.

| Name | Type | Description |
| --- | --- | --- |
| sessionId | String | Current session ID |
| batteryLevel | Number | Remaining battery<br>(four levels: 0.0, 0.33, 0.67, 1.0) |
| storageChanged | Boolean | Whether a new format storage is inserted/removed |
| \_captureStatus | String | Continuous shooting status<br>"shooting", "idle",<br>"self-timer countdown" (RICOH THETA S firmware version 01.42 or later),<br>"bracket shooting" (RICOH THETA S only; firmware version or later) |
| \_recordedTime | Number | Recorded time (sec.) of video being shot |
| \_recordableTime | Number | Remaining time (sec.) of video being shot |
| \_compositeShootingElapsedTime | Number | Elapsed time (sec.) for interval composite shooting<br>(RICOH THETA S only; firmware version 01.82 or later) |
| \_latestFileUri | String | Last saved file ID |
| \_batteryState | String | Charging status<br>"charging", "charged", "disconnect" |
| \_apiVersion | Number | Current camera API version<br>(1: v2.0, 2: v2.1)<br>(RICOH THETA S firmware version 01.62 or later) |
| \_cameraError | String Array | Camera error information (Details in the following item) |

### \_cameraError

Camera error information.

| Event flag | Error code | Description |
|:--|:--|:--|
| 0x00000001 | NO\_MEMORY | Insufficient free memory |
| 0x00000002 | WRITING\_DATA | Writing data |
| 0x00000004 | FILE\_NUMBER\_OVER | File number limit exceeded |
| 0x00000008 | NO\_DATE\_SETTING | Camera's built-in clock is not set |
| 0x00000010 | COMPASS\_CALIBRATION | Error occurred in the electromagnetic compass |
| 0x00000100 | CARD\_DETECT\_FAIL | SD Memory card is not installed |
| 0x00400000 | CAPTURE\_HW\_FAILED | Error detected in shooting hardware |
| 0x00000100 | CANT\_USE\_THIS\_CARD | Media fault |
| 0x02000000 | FORMAT\_INTERNAL\_MEM | Internal memory formatting error |
| 0x04000000 | FORMAT\_CARD | SD memory card formatting error |
| 0x08000000 | INTERNAL\_MEM\_ACCESS\_FAIL | Internal memory access error |
| 0x10000000 | CARD\_ACCESS\_FAIL | SD memory card access error |
| 0x20000000 | UNEXPECTED\_ERROR | Undefined error |
| 0x40000000 | BATTERY\_CHARGE\_FAIL | Charging error |
| 0x80000000 | HIGH\_TEMPERATURE | Temperature error |

### Example

#### Response

```
{
    "fingerprint": "12EGA33",
    "state": {
        "sessionId": "12ABC3",
        "batteryLevel": 0.33,
        "storageChanged": false,
        "_captureStatus": "idle",
        "_recordedTime": 0,
        "_recordableTime": 0,
        "_compositeShootingElapsedTime": 0,
        "_latestFileUri": "100RICOH/R0010015.JPG",
        "_batteryState": "disconnect",
        "_apiVersion": 1
    }
}
```
