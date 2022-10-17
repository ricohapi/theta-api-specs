# camera.\_listPlugins

### Overview

Acquires a list of installed plugins.

### Support model

| X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|
| All | All | v2.21.1 or later | --- | --- |

### Parameters

None.

### Results

| Name | Type | Description |
|:--|:--|:--|
| plugins | Object | Lists of the plugins installed in camera.<br>See the next section for details. |

### plugins object

| Name | Type | Description |
|:--|:--|:--|
| pluginName | String | Plugin name |
| packageName | String | Package name |
| version | String | Plugin version |
| type | String | The kind of application<br>("system": Pre-installed plugin, "user": User-added plugin) |
| running | Boolean | Plugin power status<br>(true: running, false: stop) |
| foreground | Boolean | Process status<br>(true: foreground, false: background) |
| boot | Boolean | Boot selection<br>(true: Target plugin to be started; false: Do not start this plugin) |
| force | Boolean | Reserved |
| bootOptions | String | Reserved |
| webServer | Boolean | Existence of web server<br>(true: Has WebUI, false: Does not have WebUI) |
| exitStatus | String | Exit status |
| message | String | Message |
