# camera.\_getPluginOrders

### Overview

Return the plugins for plugin mode.

### Support model

| X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|
| All | All | --- | --- | --- |

### Parameters

None.

### Results

| Name | Type | Description |
|:--|:--|:--|
| pluginOrders | String Array | For Z1, array of three package names for the start-up plugin. No restrictions for the number of package names for X. |

### Example

#### Results (RICOH THETA Z1)

```
{
    "pluginOrders":[
        "com.theta360.usbstorage",
        "com.theta.remoteplayback",
        ""
    ]
},
```
