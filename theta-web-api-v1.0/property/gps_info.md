# 0xD801 GpsInfo

### Device Prop Code

0xD801

### Overview

Acquire or set the GPS information.   
(Vendor Expansion Properties)

Return to the default value when the power is turned OFF.

### Prop Value

Current Value formats are as shown below.

\<latitude\>,\<longitude\>\<altitude\>m@\<date-time\>\<timezone\>,\<datum\>

| Field | Value | Description |
|:--|:--|:--|
| latitude | double "{\|-}nn.mmmmmm" | WGS84 / -90.000000 -- 90.000000 |
| longitude | double "{\|-}nnn.mmmmmm" | WGS84 / -180.000000 -- 180.000000 |
| altitude | double "{+\|-}nnn.mm" | Unit: Meters<br>GPSAltitudeRef 0: Height above sea level 1: Height below sea level<br>If the read value, the second decimal place might be omitted<br>(ex. read value: +999.00, set value: +999.0) |
| date-time | "YYYYMMDDThhmmss{\|.s}" | DateTime character string<br>The set value includes a decimal point. It is not included in the read value |
| timezone | "{+\|-}hhmm" or "Z" | DateTime character string<br>The only set value is supported. It is not included in the read value |
| datum | "WGS84" | Only WGS84 is supported |
