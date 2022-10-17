# 0x99AD SetAccessPointPassword

### Operation Code

0x99AD

### Overview

Sets the password for the access point used in client mode.  
(Vendor Extension Operations)

Operation parameters are as follows.

| No. | Operation Parameter | RICOH THETA Specification |
|:--|:--|:--|
| 1 | AccessPointHandle | Access point handle of the target access point |
| 2 | Reserved | unused<br>Specify 0x00000000 |
| 3 | Reserved | unused<br>Specify 0x00000000 |
| 4 | Reserved | unused<br>Specify 0x00000000 |
| 5 | Reserved | unused<br>Specify 0x00000000 |

### Support model

| X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|
| --- | All | v2.00.2 or later | --- | --- |

### Support value

The access point information format is predetermined by the following.

| Name | Size | Data Type | Description |
|:--|:--|:--|:--|
| Password | any | String | Password |
