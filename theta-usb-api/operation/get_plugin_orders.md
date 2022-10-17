# 0x99B8 GetPluginOrders

### Operation Code

0x99B8

### Overview

Return the plugins for plugin mode.  
(Vendor Extension Operations)

Operation parameters are as follows.

#### RICOH THETA X

| No. | Operation Parameter | RICOH THETA Specification |
|:--|:--|:--|
| 1 | Reserved | unused<br>Specify 0x00000000 |
| 2 | Reserved | unused<br>Specify 0x00000000 |
| 3 | Reserved | unused<br>Specify 0x00000000 |
| 4 | Reserved | unused<br>Specify 0x00000000 |
| 5 | Reserved | unused<br>Specify 0x00000000 |

Response parameters are as follows.

| No. | Response Parameter | RICOH THETA Specification |
|:--|:--|:--|
| 1 | Reserved | unused<br>Specify 0x00000000 |
| 2 | Reserved | unused<br>Specify 0x00000000 |
| 3 | Reserved | unused<br>Specify 0x00000000 |
| 4 | Reserved | unused<br>Specify 0x00000000 |
| 5 | Reserved | unused<br>Specify 0x00000000 |

The plugin handle list format is predetermined by the following.

| Name | Size | Data Type | Description |
|:--|:--|:--|:--|
| PluginHandle array | any | PluginHandle array | List of plugin handle |

A PluginHandle with an unregistered number will respond 0xFFFFFFFF.

#### RICOH THETA Z1

| No. | Operation Parameter | RICOH THETA Specification |
|:--|:--|:--|
| 1 | Reserved | unused<br>Specify 0x00000000 |
| 2 | Reserved | unused<br>Specify 0x00000000 |
| 3 | Reserved | unused<br>Specify 0x00000000 |
| 4 | Reserved | unused<br>Specify 0x00000000 |
| 5 | Reserved | unused<br>Specify 0x00000000 |

Response parameters are as follows.

| No. | Response Parameter | RICOH THETA Specification |
|:--|:--|:--|
| 1 | PluginHandle 1 | Plugin handle for Plugin 1 |
| 2 | PluginHandle 2 | Plugin handle for Plugin 2 |
| 3 | PluginHandle 3 | Plugin handle for Plugin 3 |
| 4 | Reserved | unused<br>Specify 0x00000000 |
| 5 | Reserved | unused<br>Specify 0x00000000 |

### Support model

| X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|
| All | All | --- | --- | --- |
