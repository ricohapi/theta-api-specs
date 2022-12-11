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
| 0x0001 | Normal  |
| 0x0002 | Fine    |
| 0x0003 | Economy |

| Video mode | Fine<br/>[Mbps] | Normal<br/>[Mbps] | Economy<br/>[Mbps] | Remark
|:--|:--|:--|:--|:--|
|   2K 30fps |  32 |  16 |   8 ||
|   2K 60fps |  64 |  32 |  16 ||
|   4K 10fps |  48 |  24 |  12 ||
|   4K 15fps |  64 |  32 |  16 ||
|   4K 30fps | 100 |  54 |  32 ||
|   4K 60fps | 120 |  64 |  32 ||
| 5.7K  2fps |  64 |  32 |  16 | firmware v1.40.0 or later   (I-frame only)|
|            |  16 |   8 |   4 | firmware v1.30.0 or earlier |
| 5.7K  5fps | 120 |  80 |  40 | firmware v1.40.0 or later   (I-frame only)|
|            |  32 |  16 |   8 | firmware v1.30.0 or earlier |
| 5.7K 10fps |  64 |  40 |  20 | firmware v1.40.0 or later   |
|            |  48 |  24 |  12 | firmware v1.30.0 or earlier |
| 5.7K 15fps |  64 |  32 |  16 ||
| 5.7K 30fps | 120 |  64 |  32 ||
|   8K  2fps |  64 |  32 |  16 | firmware v1.40.0 or later   (I-frame only)|
|            |  32 |  16 |   8 | firmware v1.30.0 or earlier (I-frame only)|
|   8K  5fps | 120 |  96 |  40 | firmware v1.40.0 or later   (I-frame only)|
|            |  64 |  32 |  16 | firmware v1.30.0 or earlier (I-frame only)|
|   8K 10fps | 120 |  96 |  40 | firmware v1.40.0 or later   (I-frame only)|
|            | 120 |  64 |  32 | firmware v1.30.0 or earlier (I-frame only)|

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
