# 0xD801 GpsInfo

### Device Prop Code

0xD801

### Overview

Acquire or set the GPS information.  
(Vendor Extension Property)

### Support model

| X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|
| All | All | All | All | All |

### Support value

Current Value formats are as shown below.  
If null character is set, the already configured GPS information will be deleted.

\<latitude\>,\<longitude\>\<altitude\>m@\<date-time\>\<timezone\>,\<datum\>

| Field | Value | Description |
|:--|:--|:--|
| latitude | "{\|-}nn.mmmmmm" | WGS84 / -90.000000 -- 90.000000 |
| longitude | "{\|-}nnn.mmmmmm" | WGS84 / -180.000000 -- 180.000000 |
| altitude | "{+\|-}nnnn.mm" | Unit: Meters<br>GPSAltitudeRef 0: Height above sea level 1: Height below sea level |
| date-time | "YYYYMMDDThhmmss{\|.s}" | DateTime character string<br>The set value includes a decimal point. It is not included in the read value |
| timezone | "{+\|-}hhmm" or "Z" | DateTime character string<br>The only set value is supported. It is not included in the read value |
| datum | "WGS84" | Only WGS84 is supported |
