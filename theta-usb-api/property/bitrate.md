# 0xD829 Bitrate

### Device Prop Code

0xD829

### Overview

Acquires or sets the movie bit rate.  
(Vendor Extension Property)

### Support model

| X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|
| All | All | v2.50.1 or later | --- | --- |

### Support value

#### RICOH THETA X

##### Movie shooting mode

| Value | Description |
|:--|:--|
| 0x0001 | Normal. |
| 0x0002 | High bit rate. |
| 0x0003 | Economy. |

##### Still image shooting mode

| Value | Description |
|:--|:--|
| 0x0002 | High bit rate. |

#### RICOH THETA V, Z1

| Value | Description |
|:--|:--|
| 0x0001 | Normal.<br>In movie shooting mode only. |
| 0x0002 | High bit rate.<br>In movie shooting mode only. |
| 0x0000 | Automatic.<br>In still image shooting mode or live streaming mode. |
