# State

### API

POST /osc/state

### Overview

Acquires the camera states.

Use [CheckForUpdates](check_for_updates.md) to check whether the state object has changed its contents.

### Input

None.

### Output

| Name | Type | Description |
|:--|:--|:--|
| fingerprint | String | Takes a unique value<br>per current state ID. |
| state | Object | Camera state (Refer to the next section for details.) |

### state object

State of the camera.

| Name | Type | Description |
|:--|:--|:--|
| batteryLevel | Number | Battery level<br>(0.0 to 1.0)<br>When using an external power source, 1 (100%) |
| storageUri | String | Storage URI<br>V, Z1:0 http://[IP address]/files/[eMMC ID]/<br>X: http://[IP address]/files/ |
| \_storageID \*7 | String | Storage ID |
| \_captureStatus | String | Continuously shoots state<br>"shooting", "idle", "self-timer countdown",<br>"bracket shooting" \*1, "converting"\*2, "timeShift shooting"\*7,<br>"continuous shooting"\*7, "retrospective image recording"\*7<br>(shooting: Performing continuously shoots,<br>idle: In standby,<br>self-timer countdown: Self-timer is operating,<br>bracket shooting: Performing multi bracket shooting,<br>converting: Converting post file...,<br>timeShift shooting: Performing timeShift shooting,<br>continuous shooting: Performing continuous shooting,<br>retrospective image recording: Waiting for retrospective video...) |
| \_recordedTime | Number | Shooting time of movie (sec) |
| \_recordableTime | Number | Remaining time of movie (sec) |
| \_capturedPictures \*2 | Number | Number of still images captured during continuous shooting, Unit: images |
| \_compositeShootingElapsedTime \*1\*4\*6\*8 | Number | Elapsed time for interval composite shooting (sec) |
| \_latestFileUrl | String | URL of the last saved file<br>V, Z1: http://[IP address]/files/[eMMC ID]/[Directory name]/[[File name]<br>X: http://[IP address]/files/[Directory name]/[[File name]<br>DNG format files are not displayed. For burst shooting, files in the DNG format are displayed.\*6 |
| \_batteryState | String | Charging state<br>"charging", "charged", "disconnect"<br>(charging: Charging, charged: Charging completed,<br>disconnect: Not charging) |
| \_apiVersion | Number | API version currently set<br>(1: v2.0, 2: v2.1) |
| \_pluginRunning \*3\*5 | Boolean | Plugin running state<br>(true: running, false: stop) |
| \_pluginWebServer \*3\*5 | Boolean | Plugin web server state<br>(true: enabled, false: disabled) |
| \_function \*5 | String | Shooting function status<br>"normal", "selfTimer"\*8, "mySetting" |
| \_mySettingChanged \*5 | Boolean | My setting changed state<br>(true: Shooting function status is "mySetting" and some my setting properties are changed) |
| \_currentMicrophone \*7 | String | Identifies the microphone used while recording video when _microphone option is set to "AUTO"<br>"Internal", "External"<br>(Internal: Use the built-in microphone when recording video,<br>External: Use the external microphone when recording video) |
| \_currentStorage \*7 | String | Used to identify IN/SD at the app<br>"IN", "SD"<br>(IN: Record to internal memory,<br>SD: Record to SD card) |
| \_cameraError | String Array | Error information of the camera (Refer to the next section for details.) |
| \_batterylnsert \*7 | Boolean | true: Battery inserted; false: Battery not inserted<br>If "_batteryInsert" is true, video recording via the WebAPI is restricted.<br>Video recording at 4K 60fps, 5.7K 10fps, 5.7K 15fps, 5.7K 30fps, or 8K 10fps is not possible with the WebAPI.<br>When the battery level is at the specified value or less, video recording at 4K 30fps is not possible with the WebAPI. |

\*1 RICOH THETA S firmware v01.82 or later

\*2 RICOH THETA V or later

\*3 RICOH THETA V firmware v2.21.1 or later

\*4 RICOH THETA V is not supported

\*5 RICOH THETA Z1 or later

\*6 RICOH THETA Z1

\*7 RICOH THETA X or later

\*8 RICOH THETA X is not supported

### \_cameraError

Error information of the camera

#### RICOH THETA X or later

| Event flag | Error code | Desription |
|:--|:--|:--|
| 0x00000001 | NO\_MEMORY | Insufficient memory |
| 0x00000004 | FILE\_NUMBER\_OVER | Maximum file number exceeded |
| 0x00000008 | NO\_DATE\_SETTING | Camera clock not set |
| 0x00000010 | READ\_ERROR | Includes when the card is removed |
| 0x00000020 | NOT_SUPPORTED_MEDIA_TYPE | Unsupported media (SDHC, etc.) |
| 0x00000040 | NOT_SUPPORTED_FILE_SYSTEM | FAT32, etc. |
| 0x00000100 | MEDIA_NOT_READY | Error warning while mounting |
| 0x00000200 | NOT_ENOUGH_BATTERY | Battery level warning (firmware update) |
| 0x00000400 | INVALID_FILE | Firmware file mismatch warning |
| 0x00000800 | PLUGIN_BOOT_ERROR | Plugin start warning (IoT technical standards compliance) |
| 0x00001000 | IN_PROGRESS_ERROR<br><br>CANNOT_RECORDING | When performing continuous shooting by operating the camera while executing \<Delete object\>, \<Transfer firmware file\>, \<Install plugin\> or \<Uninstall plugin\> with the WebAPI or MTP.<br><br>Battery inserted + WLAN ON + Video mode + 4K 60fps / 5.7K 10fps / 5.7K 15fps / 5.7K 30fps / 8K 10fps |
| 0x00002000 | CANNOT\_RECORD\_LOWBAT | Battery inserted AND Specified battery level or lower + WLAN ON + Video mode + 4K 30fps |
| 0x00400000 | CAPTURE\_HW\_FAILED | Shooting hardware failure |
| 0x00800000 | CAPTURE_SW_FAILED | Software error |
| 0x08000000 | INTERNAL\_MEM\_ACCESS\_FAIL | Internal memory access error |
| 0x20000000 | UNEXPECTED\_ERROR | Undefined error |
| 0x40000000 | BATTERY\_CHARGE\_FAIL | Charging error |
| 0x80000000 | HIGH\_TEMPERATURE | (Board) temperature error |
| 0x00200000 | BATTERY\_HIGH\_TEMPERATURE | Battery temperature error |

#### RICOH THETA Z1 or prior

| Event flag | Error code | Desription |
|:--|:--|:--|
| 0x00000001 | NO\_MEMORY | Insufficient memory |
| 0x00000004 | FILE\_NUMBER\_OVER | Maximum file number exceeded |
| 0x00000008 | NO\_DATE\_SETTING | Camera clock not set |
| 0x00000010 | COMPASS\_CALIBRATION | Electronic compass error |
| 0x00000800 \*1 | PLUGIN\_BOOT\_ERROR | Plugin start warning (IoT technical standards compliance) |
| 0x00400000 | CAPTURE\_HW\_FAILED | Shooting hardware failure |
| 0x08000000 | INTERNAL\_MEM\_ACCESS\_FAIL | Internal memory access error |
| 0x20000000 | UNEXPECTED\_ERROR | Undefined error |
| 0x40000000 | BATTERY\_CHARGE\_FAIL | Charging error |
| 0x80000000 | HIGH\_TEMPERATURE | (Board) temperature error |
| 0x00200000 \*1 | BATTERY\_HIGH\_TEMPERATURE | Battery temperature error |

\*1 RICOH THETA Z1 or later

### Example

#### Response

```
{
    "fingerprint": "12EGA33",
    "state": {
        "batteryLevel": 0.33,
        "storageUri": "http://192.168.1.1/files/abcde/",
        "_captureStatus": "idle",
        "_recordedTime": 0,
        "_recordableTime": 0,
        "_compositeShootingElapsedTime": 0,
        "_latestFileUrl": "http://192.168.1.1/files/abcde/100RICOH/R0010015.JPG",
        "_batteryState": "disconnect",
        "_apiVersion": 2
    }
}
```
