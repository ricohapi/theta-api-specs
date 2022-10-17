# 0x99B9 GetPluginState

### Operation Code

0x99B9

### Overview

Return the status of plugin mode.  
(Vendor Extension Operations)

Operation parameters are as follows.

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
| 1 | PluginState | Plugin mode status<br>(0: Plugin is stop, 1: Plugin is running) |
| 2 | Reserved | unused<br>Specify 0x00000000 |
| 3 | Reserved | unused<br>Specify 0x00000000 |
| 4 | Reserved | unused<br>Specify 0x00000000 |
| 5 | Reserved | unused<br>Specify 0x00000000 |

### Support model

| X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|
| All | All | v3.00.1 or later | --- | --- |
