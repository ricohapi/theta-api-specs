# \_autoBracket

### Overview

Multi bracket shooting setting.   
(RICOH THETA S firmware v01.82 or later and RICOH THETA SC firmware v1.10 or later only)

Can be acquired by [camera.getOptions](../commands/camera.get_options.md) and set by [camera.setOptions](../commands/camera.set_options.md).

\_bracketNumber is the only supported value that can be acquired by [camera.getOptions](../commands/camera.get_options.md).

### Support value

| Key | Description |
|:--|:--|
| \_bracketNumber | Number of shots in multi bracket shooting.<br>2 to 13. |
| \_bracketParameters | Parameter array specified for multi bracket shooting.<br>Specify [iso](iso.md), [shutterSpeed](shutter_speed.md), and [\_colorTemperature](_color_temperature.md). |

### Example

#### Options

```
{
    "_autoBracket": {
        "_bracketNumber": 3,
        "_bracketParameters": [
            {
                "shutterSpeed": 0.004,
                "iso": 400,
                "_colorTemperature": 5100
            },
            {
                "shutterSpeed": 0.004,
                "iso": 320,
                "_colorTemperature": 5100
            },
            {
                "shutterSpeed": 0.004,
                "iso": 2500,
                "_colorTemperature": 5000
            }
        ]
    }
}
```
