# 0x99BF GetAccessPointProxy

### Operation Code

0x99BF

### Overview

Return the proxy information registered in the access point.
(Vendor Extension Operations)

Operation Parameters as follows

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

The access point proxy format is predetermined by the following.

\<Use\>\<Url\>\<Port\>\<UserID\>

| Name | Size | Data Type | Description |
|:--|:--|:--|:--|
| Use | 1 | UINT8 | Presence of proxy usage <br> (0: do not use proxy, 1: use proxy) |
| Url | 64 | String | Proxy server URL |
| Port | 5 | String | Proxy server port number: 0 to 65535 |
| UserID | 64 | String | User ID used for proxy authentication |
