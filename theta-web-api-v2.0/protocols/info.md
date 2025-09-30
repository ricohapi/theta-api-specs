# Info

### API

GET /osc/info

### Overview

Acquires basic information about the camera and supported function.

### Input

None.

### Output

| Name | Type | Description |
|:--|:--|:--|
| manufacturer | String | Manufacturer name |
| model | String | Model number |
| serialNumber | String | Serial number |
| firmwareVersion | String | Firmware version |
| supportUrl | String | Support page URL |
| gps | Boolean | Existence of GPS |
| gyro | Boolean | Existence of gyroscope |
| uptime | Integer | Time elapsed after startup (sec.) |
| api | String Array | List of supported API |
| endpoints | Object | End point information (Details in the following item) |
| apiLevel | Integer Array | Supported API version<br>(1: v2.0, 2: v2.1)<br>(RICOH THETA S firmware version 01.62 and later) |

### endpoints Object

End point information.

| Name | Type | Description |
|:--|:--|:--|
| httpPort | Integer | Port number used by API |
| httpUpdatesPort | Integer | Port number when status check update ([CheckForUpdates](check_for_updates.md)) |

### Example

#### Response

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
