# \_autoBracket

### Overview

Multi bracket shooting setting.

Can be acquired by [camera.getOptions](../commands/camera.get_options.md) and set by [camera.setOptions](../commands/camera.set_options.md).

\_bracketNumber is the only supported value that can be acquired by [camera.getOptions](../commands/camera.get_options.md).  

For "_bracketParameters", all parameters must be specified.

### Support model

| X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|
| All | All | All | v1.10 or later | v01.82 or later |

### Support value

| Key | Description |
|:--|:--|
| \_bracketNumber | Number of shots in multi bracket shooting.<br>2 to 13 (RICOH THETA V firmware v2.50.1  or prior, RICOH THETA X); 2 to 19 (RICOH THETA V firmware v3.00.1 or after). |
| \_bracketParameters | Parameter array specified for multi bracket shooting.<br>Specify [iso](iso.md), [shutterSpeed](shutter_speed.md), and [\_colorTemperature](_color_temperature.md) for RICOH THETA V firmware v2.50.1 or prior;<br>or specify [iso](iso.md) \*1, [shutterSpeed](shutter_speed.md) \*1, [\_colorTemperature](_color_temperature.md) \*1, [exposureProgram](exposure_program.md) \*3, [aperture](aperture.md) \*1\*2, [exposureCompensation](exposure_compensation.md) \*1, and [whiteBalance](white_balance.md) for RICOH THETA V firmware v3.00.1 or later. |

\*1: Optional<br>
\*2: Only RICOH THETA Z1 supports `aperture` option.  
\*3: RICOH THETA X supports only `1` (Manual program).

### Example

#### Options (for RICOH THETA V firmware v2.50.1 or prior)

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

#### Options (for RICOH THETA V firmware v3.00.1 or later)

```
{
    "_autoBracket": {
        "_bracketNumber": 2,
        "_bracketParameters": [
            {
                "aperture": 2.0,
                "_colorTemperature": 5000,
                "exposureCompensation": 0,
                "exposureProgram": 1,
                "iso": 400,
                "shutterSpeed": 0.004,
                "whiteBalance": "auto"
            },
            {
                "aperture": 2.0,
                "_colorTemperature": 5000,
                "exposureCompensation": 0,
                "exposureProgram": 1,
                "iso": 400,
                "shutterSpeed": 0.004,
                "whiteBalance": "auto"
            }
        ]
    }
}
```
\* Values that correspond to options are different for each model so refer to the page describing each option for details.
