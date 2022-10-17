# gpsInfo

### Overview

GPS location information.

In order to append the location information, this property should be specified by the client.

The current setting can be acquired by [camera.getOptions](../commands/camera.get_options.md), and it can be changed by [camera.setOptions](../commands/camera.set_options.md).

### Support model

| X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|
| All | All | All | All | All |

### Support value

| Key | Description |
|:--|:--|
| lat | Latitude (-90.000000 -- 90.000000)<br>When GPS is disabled: 65535 \*1\*2 |
| lng | Longitude (-180.000000 -- 180.000000)<br>When GPS is disabled: 65535 \*1\*2 |
| \_altitude | Altitude (meters)<br>When GPS is disabled: 0 \*1\*2 |
| \_dateTimeZone | Location information acquisition time<br>YYYY:MM:DD hh:mm:ss+(-)hh:mm<br>hh is in 24-hour time, +(-)hh:mm is the time zone<br>when GPS is disabled: ""(Null characters) \*1\*2 |
| \_datum | Geodetic reference<br>When GPS is enabled: WGS84<br>When GPS is disabled: ""(Null characters) \*1\*2 |

\*1 65535 is set for lat and lng when disabling the GPS setting at RICOH THETA Z1 and prior.  
\*2 For RICOH THETA X, ON/OFF for assigning position information is set at [_gpsTagRecording](_gps_tag_recording.md).

### Example

#### Options

```
{
    "gpsInfo": {
        "lat": 23.532,
        "lng": 23.532,
        "_altitude": 999.00,
        "_dateTimeZone": "2014:05:18 01:04:29+08:00",
        "_datum": "WGS84"
    }
}
```
