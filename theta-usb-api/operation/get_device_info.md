# 0x1001 GetDeviceInfo

### Operation Code

0x1001

### Overview

Return device information data.

Changes in the device information associated with the property change of [FunctionalMode](../property/functional_mode.md) property are notified by [DeviceInfoChanged](../event/device_info_changed.md) event.

Details of each Dataset field are as follows.

| Name | RICOH&nbsp;THETA Specification |
|:--|:--|
| vendor\_extension\_id | Fixed value irrespective of the firmware version |
| vendor\_extension\_version | RICOH THETA Camera version<br>110 (RICOH THETA S or later) |
| device\_version | RICOH THETA firmware version. For details of the revision history, see the download page on theta360.com |
| serial\_number | RICOH THETA camera serial number |
| functional\_mode | Camera status ([FunctionalMode](../property/functional_mode.md)) |

### Support model

| X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|
| All | All | All | All | All |

