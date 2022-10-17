# 0x99B6 GetBluetoothMacAddress

### Operation Code

0x99B6

### Overview

Return the MAC address of Bluetooth.  
(Vendor Extension Operations)

Operation parameters as follows.

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
| All | All | v2.11.1 or later | --- | --- |

### Support value

The MAC address format is predetermined by the following.

| Name | Size | Data Type | Description |
|:--|:--|:--|:--|
| MacAddress | 18 | String | MAC address |
