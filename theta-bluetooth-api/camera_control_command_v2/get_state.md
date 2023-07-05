# Get State

### Service

b6ac7a7e-8c01-4a52-b188-68d53df53ea2

### Characteristic

083d92b0-21e0-4fb2-9503-7d8b2c2bb1d1

### Format

utf8s

### Overview

Acquires the camera states.

### Value Fields

| Name| Type | Description |
|:--|:--|:--|
| batteryLevel | Number | Battery level<br>(0.0 to 1.0)<br>When using an external power source, 1 (100%) |
| \_captureStatus | String | Continuously shoots state<br>"shooting", "idle", "self-timer countdown",<br>"bracket shooting", "converting", "timeShift shooting"\*2,<br>"continuous shooting"\*2, "retrospective image recording"\*2<br>(shooting: Performing continuously shoots,<br>idle: In standby,<br>self-timer countdown: Self-timer is operating,<br>bracket shooting: Performing multi bracket shooting,<br>converting: Converting post file...,<br>timeShift shooting: Performing timeShift shooting,<br>continuous shooting: Performing continuous shooting,<br>retrospective image recording: Waiting for retrospective video...) |
| \_recordedTime | Number | Shooting time of movie (sec) |
| \_recordableTime | Number | Remaining time of movie (sec) |
| \_capturedPictures | Number | Number of still images captured during continuous shooting, Unit: images |
| \_latestFileUrl | String | URL of the last saved file<br>Z1: http://[IP address]/files/[eMMC ID]/[Directory name]/[[File name]<br>X: http://[IP address]/files/[Directory name]/[[File name]<br>DNG format files are not displayed. For burst shooting, files in the DNG format are displayed.\*1 |
| \_batteryState | String | Charging state<br>"charging", "charged", "disconnect"<br>(charging: Charging, charged: Charging completed,<br>disconnect: Not charging) |
| \_function | String | Shooting function status<br>"normal", selfTimer"\*8, "mySetting" |
| \_cameraError | String Array | Error information of the camera (Refer to the next section for details.) |
| \_batterylnsert \*2 | Boolean | true: Battery inserted; false: Battery not inserted|
| \_boardTemp | Number | Camera main board temperature |
| \_batteryTemp | Number | Battery temperature |

\*1 RICOH THETA Z1

\*2 RICOH THETA X or later

```
Response (for RICOH THETA X)
{
    "_batteryInsert": true,
    "batteryLevel": 0.97,
    "_batteryState": "charging",
    "_cameraError": ["NO_DATE_SETTING"],
    "_captureStatus": "idle",
    "_capturedPictures": 0,
    "_function": "normal",
    "_latestFileUrl": "",
    "_recordableTime": 3844,
    "_recordedTime": 0,
    "_batteryTemp": 29,
    "_boardTemp": 28,
}
```

### Properties

| Property | Requirement |
|:--|:--|
| Read | Mandatory |
| Write | Excluded |
| Notify | Excluded |
