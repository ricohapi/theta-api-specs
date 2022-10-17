# 0x99A8 GetPluginHandles

### Operation Code

0x99A8

### Overview

Return the plugin handle list.  
(Vendor Extension Operations)

Operation parameters are as follows.

| No. | Operation Parameter | RICOH THETA Specification |
|:--|:--|:--|
| 1 | Reserved | unused<br>Specify 0x00000000 |
| 2 | Reserved | unused<br>Specify 0x00000000 |
| 3 | Reserved | unused<br>Specify 0x00000000 |
| 4 | Reserved | unused<br>Specify 0x00000000 |
| 5 | Reserved | unused<br>Specify 0x00000000 |

### Support model

| X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|
| --- | All | v2.21.1 or later | --- | --- |

### Support value

The plugin handle list format is predetermined by the following.

| Name | Size | Data Type | Description |
|:--|:--|:--|:--|
| PluginHandle array | any | PluginHandle array | List of plugin handle |
