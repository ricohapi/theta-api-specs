# 0x99C1 SetAccessPointProxyPassword

### Operation Code

0x99C1

### Overview

Set the password for the proxy information of the access point being used in client mode.
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
| --- | v2.20.3 or later | --- | --- | --- |

### Support value

The proxy password format is predetermined by the following.

| Name | Size | Data Type | Description |
|:--|:--|:--|:--|
| ProxyPassword | 64 | String | Password used for proxy authentication. |
