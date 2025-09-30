# camera.\_getMySetting

### Overview

Acquires the shooting properties set by the [camera.\_setMySetting](camera._set_my_setting.md) command.

Refer to My Settings in [Options Overview](../options.md) for properties available for acquisition.

### Support model

| X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|
| All | All | v2.30.1 and later | v1.10 and later | v01.82 and later |

### Parameters

| Name | Type | Description |
|:--|:--|:--|
| mode | String | The target shooting mode.<br>RICOH THETA V firmware v2.30.1 and later.<br>("image": still image capture mode, "video": video capture)<br>In RICOH THETA S and SC, do not set then it can be acquired for still image. |
| optionNames | String Array | List of option names to acquire in the JSON format.<br>Set to RICOH THETA S or SC only.<br>In another model, do not set then all properties are acquired. |

### Results

| Name | Type | Description |
|:--|:--|:--|
| options | Object | Names of the options specified for acquisition in the JSON format and the set of current values |

### Example (RICOH THETA S or SC)

#### Parameters

```
{
    "optionNames": [
        "_filter",
        "exposureProgram"
    ]
}
```

#### Results

```
{
    "options": {
         "_filter": "DR Comp",
         "exposureProgram": 2
    }
}
```
