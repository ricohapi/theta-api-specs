# OpenPluginPage

### API

GET /plugin

### Overview

Open plugin web page.

For RICOH THETA Z1 and later, specify the target plugin as a query "id=\<PluginOrder Number\>" (Z1:\<[PluginOrder](../commands/camera._set_plugin_orders.md) Number\> = 1, 2 or 3, X:\<[PluginOrder](../commands/camera._set_plugin_orders.md) Number\> = 1, 2,,,,,n) to the URL when [\_pluginRunning](state.md) is stop.

### Support model

| X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|
| All | All | v2.21.1 and later | --- | --- |

### Input

None.

### Output

HTML data of plugin web page.
