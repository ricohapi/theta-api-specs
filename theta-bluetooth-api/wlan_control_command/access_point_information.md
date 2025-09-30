# Access Point Information

### Service

F37F568F-9071-445D-A938-5441F2E82399

### Characteristic

474478B8-3A86-4DAB-AF4E-F0E2C69AFA33

### Overview

Acquires the detailed access point information applicable in [Selected Access Point](selected_access_point.md).  
 RICOH THETA V firmware v2.00.2 and later.

### Value Fields

| Name | Type | Description |
|:--|:--|:--|
| SSID Length | sint8 | SSID length |
| SSID | utf8s | SSID |
| SSID Stealth | sint8 | SSID stealth<br>(0: Disabled, 1: Enabled) |
| Security | sint8 | Authentication mode<br>(0: None, 1: WEP, 2: WPA/WPA2 PSK) |
| Connection Priority | sint8 | Connection priority |
| IP Address Allocation | sint8 | IP address allocation<br>(0: Dynamic, 1: Static) |
| IP Address | sint32 | IP address assigned to camera<br>This setting can be acquired when "IP Address Allocation" is "Static" |
| Subnet Mask | sint32 | Subnet mask<br>This setting can be acquired when "IP Address Allocation" is "Static" |
| Default Gateway | sint32 | Default gateway<br>This setting can be acquired when "IP Address Allocation" is "Static" |

### Properties

| Property | Requirement |
|:--|:--|
| Read | Mandatory |
| Write | Excluded |
| Notify | Excluded |
