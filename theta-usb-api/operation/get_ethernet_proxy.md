# 0x99C2 GetEthernetProxy

### Operation Code

0x99C2

### Overview

Return the proxy information to be used when wired LAN is enabled.
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
| --- | v2.20.3 or later | --- | --- | --- |

### Support value

The proxy dataset format is predetermined by the following.

\<Use\>\<Url\>\<Port\>\<UserID\>

| Name | Size | Data Type | Description |
|:--|:--|:--|:--|
| Use | 1 | UINT8 | Presence of proxy usage <br> (0: do not use proxy, 1: use proxy) |
| Url | 64 | String | Proxy server URL |
| Port | 5 | String | Proxy server port number: 0 to 65535 |
| UserID | 64 | String | User ID used for proxy authentication |
