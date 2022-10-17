# camera.\_pluginControl

### Overview

Starts or stops plugin.

### Support model

| X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|
| All | All | v2.21.1 or later | --- | --- |

### Parameters

#### For RICOH THETA Z1 or later

| Name | Type | Description |
|:--|:--|:--|
| action | String | Kind of action.<br>("boot": start plugin; "finish": stop) |
| plugin | String | (Optional)<br>Target plugin package name<br>If no target is specified, then Plugin 1 will start. This parameter is ignored when action parameter is "finish". |

#### For RICOH THETA V

| Name | Type | Description |
|:--|:--|:--|
| action | String | Kind of action. Target is the plugin which boot selection is true in [camera.\_listPlugins](camera._list_plugins.md)<br>("boot": start plugin; "finish": stop) |

### Results

None.
