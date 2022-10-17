# camera.\_setPluginOrders

### Overview

Sets the plugins for plugin mode.

### Support model

| X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|
| All | All | --- | --- | --- |

### Parameters

| Name | Type | Description |
|:--|:--|:--|
| pluginOrders | String Array | For Z1, array of three package names for the start-up plugin. No restrictions for the number of package names for X.<br>When not specifying, set an empty string. If an empty string is placed mid-way, it will be moved to the front.<br>Specifying zero package name will result in an error. |

### Results

None.

### Example

#### Parameters

In the case when 1: "com.theta360.usbstorage", 2: "com.theta.remoteplayback", 3: disabled

```
{
    "pluginOrders": [
        "com.theta360.usbstorage",
        "com.theta.remoteplayback",
        ""
    ]
}
```
