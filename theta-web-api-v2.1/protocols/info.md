# Info

### API

GET /osc/info

### Overview

Acquires basic information of the camera and supported functions.

### Input

None.

### Output

| Name | Type | Description |
|:--|:--|:--|
| manufacturer | String | Manufacturer name |
| model | String | Model |
| serialNumber | String | Serial number |
| \_wlanMacAddress | String | MAC address of wireless LAN (\*1)<br>(RICOH THETA V firmware v2.11.1 and later) |
| \_bluetoothMacAddress | String | MAC address of Bluetooth<br>(RICOH THETA V firmware v2.11.1 and later) |
| firmwareVersion | String | Firmware version |
| supportUrl | String | URL of the support page |
| gps | Boolean | Presence of GPS |
| gyro | Boolean | Presence of gyroscope |
| uptime | Integer | Elapsed time after startup (sec) |
| api | String Array | List of supported APIs |
| endpoints | Object | Endpoint information (Refer to the next section for details.) |
| apiLevel | Integer Array | List of supported APIs<br>(1: v2.0, 2: v2.1) |

(\*1) For THETA X, firmware versions v2.63.0 and earlier display `the communication MAC address`, while v2.71.1 and later diplay `the physical MAC address`. For other than THETA X, `the physical MAC address` is displayed.  

### endpoints object

Endpoint information

| Name | Type | Description |
|:--|:--|:--|
| httpPort | Integer | Port number for using APIs |
| httpUpdatesPort | Integer | Port number for status update check ([CheckForUpdates](check_for_updates.md)) |

### Example

#### Response (for RICOH THETA V)

```
{
        "manufacturer": "RICOH",
        "model": "RICOH THETA S",
        "serialNumber": "00001234",
        "firmwareVersion": "1.62",
        "supportUrl": "https://theta360.com/en/support/",
        "apiLevel": [1, 2],
        "endpoints": {
            "httpPort": 80,
            "httpUpdatesPort": 80
        },
        "gps": false,
        "gyro": false,
        "uptime": 67,
        "api": [
            "/osc/info",
            "/osc/state",
            "/osc/checkForUpdates",
            "/osc/commands/execute",
            "/osc/commands/status"
        ]
}
```
