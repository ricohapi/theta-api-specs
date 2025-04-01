# 0x99AB PluginControl

### Operation Code

0x99AB

### Overview

Starts or stops plugin.  
(Vendor Extension Operations)

Operation Parameters as follows.

#### For RICOH THETA Z1 or later

| No. | Operation Parameter | RICOH THETA Specification |
|:--|:--|:--|
| 1 | Type | Kind of action.<br>(0: start plugin; 1: stop) |
| 2 | PluginHandle | Target plugin handle.<br>If no target is specified, then PluginHandle 1 of [SetPluginOrders](set_plugin_orders.md) will start. This parameter is ignored when action parameter is 1 (stop). |
| 3 | Reserved | unused<br>Specify 0x00000000 |
| 4 | Reserved | unused<br>Specify 0x00000000 |
| 5 | Reserved | unused<br>Specify 0x00000000 |

#### For RICOH THETA V

| No. | Operation Parameter | RICOH THETA Specification |
|:--|:--|:--|
| 1 | Type | Kind of action. Target is the plugin which boot selection is true in [GetPluginInfo](get_plugin_info.md)<br>(0: start plugin; 1: stop) |
| 2 | Reserved | unused<br>Specify 0x00000000 |
| 3 | Reserved | unused<br>Specify 0x00000000 |
| 4 | Reserved | unused<br>Specify 0x00000000 |
| 5 | Reserved | unused<br>Specify 0x00000000 |

### Support model

| X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|
| All | All | v2.21.1 or later | --- | --- |
