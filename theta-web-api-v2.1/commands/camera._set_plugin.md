# camera.\_setPlugin

### Overview

Sets the installed pugin for boot.

For RICOH THETA Z1 or later, use [camera.\_setPluginOrders](camera._set_plugin_orders.md).

### Support model

| X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|
| All | All | v2.21.1 or later | --- | --- |

### Parameters

| Name | Type | Description |
|:--|:--|:--|
| packageName | String | Target package name for boot |
| boot | Boolean | *Valid only for V<br>Boot selection<br>Specify true |
| force | Boolean | Starts the specified plug-in when the power is turned on from power off or sleep.This setting can only be enabled for one plugin and defaults to false.<br>*After enabling this option, the specified plugin will always start. Make sure that the plug-in that specifies this option can start and stop correctly before setting it. |
| bootOptions | String | An option to pass to the plugin when the plugin starts. The initial value is NULL and the maximum is 1536 characters. |

### Results

None.

