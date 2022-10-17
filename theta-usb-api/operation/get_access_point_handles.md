# 0x99A3 GetAccessPointHandles

### Operation Code

0x99A3

### Overview

Return the access point handle list used in client mode.  
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
| --- | All | v2.00.2 or later | --- | --- |

### Support value

The access point handle list format is predetermined by the following.

| Name | Size | Data Type | Description |
|:--|:--|:--|:--|
| AccessPointHandle array | any | AccessPointHandle array | List of access point handle |
