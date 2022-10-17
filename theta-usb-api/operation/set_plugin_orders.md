# 0x99B7 SetPluginOrders

### Operation Code

0x99B7

### Overview

Sets the plugins for plugin mode.  
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

The plugin handle list format is predetermined by the following.

| Name | Size | Data Type | Description |
|:--|:--|:--|:--|
| PluginHandle array | any | PluginHandle array | List of plugin handle |

1. Register with the order for plugins specified with the PluginHandle array.  
2. Set 0xFFFFFFFF as a PluginHandle for non-registered numbers. 
3. Plugins specified in the n-th element of the array are registered in n+1.  
4. When a plugin not specified in this API is already registered on the camera side, a plugin specified in this API is set from the start.


#### RICOH THETA Z1

| No. | Operation Parameter | RICOH THETA Specification |
|:--|:--|:--|
| 1 | PluginHandle 1 | Plugin handle to be set Plugin 1 |
| 2 | PluginHandle 2 | Plugin handle to be set Plugin 2 |
| 3 | PluginHandle 3 | Plugin handle to be set Plugin 3 |
| 4 | Reserved | unused<br>Specify 0x00000000 |
| 5 | Reserved | unused<br>Specify 0x00000000 |

When not specifying, set 0xFFFFFFFF. If 0xFFFFFFFF is placed mid-way, it will be moved to the front.  
Specifying zero plugin will result in an error.

### Support model

| X | Z1 | V | SC | S |
| --- | --- | --- | --- | --- |
| All | All | --- | --- | --- |
