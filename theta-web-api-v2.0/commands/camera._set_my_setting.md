# camera.\_setMySetting

### Overview

Sets the still image shooting properties upon startup.   
(For RICOH THETA S firmware v01.82 and later and RICOH THETA SC firmware v1.10 and later only)  
To adjust the properties, use [camera.setOptions](camera.set_options.md).

Refer to My Settings in [Options Overview](../options.md) for properties which can be set.

### Parameters

| Name | Type | Description |
|:--|:--|:--|
| options | Object | Names of the options specified for acquisition in the JSON format and the set of current values.<br>Values supported in the still image shooting mode are only available for [fileFormat](../options/file_format.md). |

### Results

None

### Example

#### Parameters

```
{
    "options": {
        "_filter": "Noise Reduction",
        "exposureProgram": 2
    }
}
```
