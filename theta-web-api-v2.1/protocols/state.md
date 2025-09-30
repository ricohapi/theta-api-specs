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
| \_latestFileUrl | String | URL of the last saved file<br>V, Z1: http://[IP address]/files/[eMMC ID]/[Directory name]/[File name]<br>X: http://[IP address]/files/[Directory name]/[File name]<br>DNG format files are not displayed. For burst shooting, files in the DNG format are displayed.\*6 |
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
| \_externalGpsInfo \*9\*10 | Object | Location data is obtained through an external device using WebAPI or BLE-API.<br>Please refer to the object specification for [gpsInfo](../options/gps_info.md) as well. |
| \_internalGpsInfo \*9\*10 | Object | Location data is obtained through an internal GPS module.<br>Please refer to the object specification for [gpsInfo](../options/gps_info.md) as well.<br>RICOH THETA Z1 does not have a built-in GPS module. |
| \_boardTemp \*9\*10 | Number | This represents the current temperature inside the camera as an integer value, ranging from -10°C to 100°C with a precision of 1°C. | 
| \_batteryTemp \*9\*10 | Number | This represents the current temperature inside the battery as an integer value, ranging from -10°C to 100°C with a precision of 1°C. |

\*1 RICOH THETA S firmware v01.82 and later

\*2 RICOH THETA V and later

\*3 RICOH THETA V firmware v2.21.1 and later

\*4 RICOH THETA V is not supported

\*5 RICOH THETA Z1 and later

\*6 RICOH THETA Z1

\*7 RICOH THETA X and later

\*8 RICOH THETA X is not supported

\*9 RICOH THETA X firmware v2.20.1 and later

\*10 RICOH THETA Z1 firmware v3.10.2 and later

### \_cameraError

Error information of the camera

#### RICOH THETA X

| Error code | Can/not shoot | Desription | Recommended action |
|:--|:-:|:--|:--|
| NO\_MEMORY         | |Insufficient memory | Delete files |
| FILE\_NUMBER\_OVER | | Maximum file number exceeded | Delete 999 folder or delete 9999 file |
| NO\_DATE\_SETTING  | ✓ | Camera clock not set | Set Date/Time via API, UI, or NTP |
| ELECTRONIC\_COMPASS\_CALIBRATION \*2  | ✓ | Electronic compass error | Move the camera with ∞ pattern |
| READ\_ERROR               | ✓ | Includes when the card is removed | Change or format the microSD card |
| NOT_SUPPORTED_MEDIA_TYPE  | ✓ | Unsupported media (SDHC, etc.) | Use microSDXC card |
| NOT_SUPPORTED_FILE_SYSTEM | ✓ | Unsupported format (FAT32, etc.) | Format the microSD card |
| MEDIA_NOT_READY           | ✓ | Error warning while mounting | Wait for the microSD card is mounted |
| NOT_ENOUGH_BATTERY | ✓ | Battery level warning (firmware update) | Charge battery |
| INVALID_FILE       | ✓ | Firmware file mismatch warning | Retry firmware update |
| PLUGIN_BOOT_ERROR  | ✓ | Plugin start warning (IoT technical standards compliance) | Disconnect from internet |
| IN_PROGRESS_ERROR  | | When performing continuous shooting by operating the camera while executing \<Delete object\>, \<Transfer firmware file\>, \<Install plugin\> or \<Uninstall plugin\> with the WebAPI or MTP. | Wait for the processing finished |
| CANNOT_RECORDING   | | Battery inserted + WLAN ON + Video mode + 4K 60fps / 5.7K 10fps / 5.7K 15fps / 5.7K 30fps / 8K 10fps | Turn off WLAN |
| CANNOT\_RECORD\_LOWBAT | | Battery inserted AND Specified battery level or lower + WLAN ON + Video mode + 4K 30fps | Charge the battery |
| CAPTURE\_HW\_FAILED | | Shooting hardware failure | Reboot the camera may help |
| CAPTURE_SW_FAILED   | | Software error | Reboot the camera may help |
| INTERNAL\_MEM\_ACCESS\_FAIL | | Internal memory access error | Reboot the camera may help |
| UNEXPECTED\_ERROR   | | Undefined error | Reboot the camera may help |
| BATTERY\_CHARGE\_FAIL | | Charging error | Check USB cable or charger |
| HIGH\_TEMPERATURE\_WARNING \*1 | ✓ | (Board) temperature warning | Cool the camera |
| HIGH\_TEMPERATURE          | | (Board) temperature error | Cool the camera |
| BATTERY\_HIGH\_TEMPERATURE | | Battery temperature error | Cool the camera |

\*1 RICOH THETA X firmware v1.40.0 and later  
\*2 RICOH THETA X firmware v2.40.0 and later

#### RICOH THETA Z1 and earlier

| Error code | Can/not shoot | Desription | Recommended action |
|:--|:-:|:--|:--|
| NO\_MEMORY | | Insufficient memory | Delete files |
| FILE\_NUMBER\_OVER | | Maximum file number exceeded | Delete 999 folder or delete 9999 file |
| NO\_DATE\_SETTING  | ✓ | Camera clock not set | Set Date/Time via API |
| ELECTRONIC\_COMPASS\_CALIBRATION | ✓ | Electronic compass error | Move the camera with ∞ pattern |
| PLUGIN\_BOOT\_ERROR \*1 | ✓ | Plugin start warning (IoT technical standards compliance) | Disconnect from internet |
| HIGH\_TEMPERATURE\_WARNING \*2 | ✓ | (Board) temperature warning | Cool the camera |
| CAPTURE\_HW\_FAILED | | Shooting hardware failure | Reboot the camera may help |
| INTERNAL\_MEM\_ACCESS\_FAIL | | Internal memory access error | Reboot the camera may help |
| UNEXPECTED\_ERROR | | Undefined error | Reboot the camera may help |
| BATTERY\_CHARGE\_FAIL | | Charging error | Check USB cable or charger |
| HIGH\_TEMPERATURE | | (Board) temperature error | Cool the camera |
| BATTERY\_HIGH\_TEMPERATURE \*1 |  | Battery temperature error | Cool the camera |

\*1 RICOH THETA Z1 and later  
\*2 RICOH THETA Z1 v2.20.3 and later  

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
