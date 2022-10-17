# camera.\_getMySetting

### Overview

Acquires the still image shooting properties set by the [camera.\_setMySetting](camera._set_my_setting.md) command.   
(RICOH THETA S firmware v01.82 or later and RICOH THETA SC firmware v1.10 or later only)

Refer to My Settings in [Options Overview](../options.md) for properties available for acquisition.

### Parameters

| Name | Type | Description |
|:--|:--|:--|
| optionNames | String Array | List of option names to acquire in the JSON format |

### Results

| Name | Type | Description |
|:--|:--|:--|
| options | Object | Names of the options specified for acquisition in the JSON format and the set of current values |

### Example

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
