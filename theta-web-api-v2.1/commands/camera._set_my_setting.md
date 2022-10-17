# camera.\_setMySetting

### Overview

Registers shooting conditions in My Settings.  
To adjust the properties, use [camera.setOptions](camera.set_options.md).  
The properties can be reset to the default values by [camera.reset](camera.reset.md).

Conditions registered in My Settings are updated when the camera is turned on for RICOH THETA V or prior.   
Conditions registered in My Settings are updated when switching to My Settings mode for RICOH THETA Z1 or later.

Refer to My Settings in [Options Overview](../options.md) for properties which can be set.

### Support model

| X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|
| All | All | v2.30.1 or later | v1.10 or later | v01.82 or later |

### Parameters

| Name | Type | Description |
|:--|:--|:--|
| mode | String | The target shooting mode.<br>RICOH THETA V firmware v2.30.1 or later.<br>("image": still image capture mode, "video": video capture)<br>In RICOH THETA S and SC, do not set then it can be acquired for still image. |
| options | Object | Names of the options specified for acquisition in the JSON format and the set of current values. |

#### Note (RICOH THETA V only. Firmware v3.00.1 or later.)

The following persistence options can be set the choice "Do not update My Setting condition on power-on."   
In that case, the camera will start up with the option values stored on turn-off even if another My Setting condition is registered.

| Option name | Choise "Do not update My Setting condition" |
|:--|:--|
| exposureDelay | -1 |
| \_maxRecordableTime | -1 |
| fileFormat | {"type":"jpeg", "width":0, "height":0} (for image mode)<br>{"type":"mp4", "width":0, "height":0} (for video mode) |
| isoAutoHighLimit | -1<br>(RICOH THETA V firmware v3.03.1 or later) |

### Results

None

### Example (RICOH THETA S or SC)

#### Parameters

```
{
    "options": {
        "_filter": "Noise Reduction",
        "exposureProgram": 2
    }
}
```
