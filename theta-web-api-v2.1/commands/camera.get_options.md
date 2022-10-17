# camera.getOptions

### Overview

Acquires the properties and property support specifications for shooting, the camera, etc.

Refer to the options category of API v2.1 reference for details on properties that can be acquired.

The support specifications for each property can be acquired using the property name + "Support" name.   
E.g. "iso" support specifications property name: "isoSupport"

There is a detailed example of the request in [Getting Started.](../getting_started.md#3-acquire-and-set-properties)

### Parameters

| Name | Type | Description |
|:--|:--|:--|
| optionNames | String Array | JSON format option name list to be acquired |

### Results

| Name | Type | Description |
|:--|:--|:--|
| options | Object | Set of option names and current values or support values specified to be acquired in JSON format |

### Example

#### Parameters

```
{
    "optionNames": [
        "iso",
        "isoSupport"
    ]
}
```

#### Results

```
{
    "options": {
         "iso": 200,
         "isoSupport": [100, 200, 400, 800, 1600]
    }
}
```
