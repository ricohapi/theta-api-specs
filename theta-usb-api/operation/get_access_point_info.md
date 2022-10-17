# 0x99A4 GetAccessPointInfo

### Operation Code

0x99A4

### Overview

Return the detailed access point information used in client mode.  
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
| ---| All | v2.00.2 or later | --- | --- |

### Support value

The access point information format is predetermined by the following.

\<SSID\>\<SSID Stealth\>\<Security\>\<ConnectionPriority\>\<IpAddressAllocation\>\<IPAddress\>\<SubnetMask\>\<DefaultGateway\>

| Name | Size | Data Type | Description |
|:--|:--|:--|:--|
| SSID | any | String | SSID |
| SSID Stealth | 1 | UINT8 | SSID stealth<br>(0: Disabled, 1: Enabled) |
| Security | any | String | Authentication mode<br>("none", "WEP", "WPA/WPA2 PSK") |
| ConnectionPriority | 1 | UINT8 | Connection priority |
| IpAddressAllocation | 1 | UINT8 | IP address allocation<br>(0: Dynamic, 1: Static) |
| IPAddress | 4 | UINT32 | IP address assigned to camera<br>This can be acquired when IpAddressAllocation is "Static" |
| SubnetMask | 4 | UINT32 | Subnet mask<br>This can be acquired when IpAddressAllocation is "Static" |
| DefaultGateway | 4 | UINT32 | Default gateway<br>This can be acquired when IpAddressAllocation is "Static" |
