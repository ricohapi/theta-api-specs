# 0xD839 BurstOption

### Device Prop Code

0xD839

### Overview

Burst shooting setting.  
(Vendor Extension Property)

### Support model

| X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|
| --- | v2.10.1 or later | --- | --- | --- |

### Support value

Current Value formats are as shown below.  

\<burstCaptureNum\>,\<burstBracketStep\>,\<burstCompensation\>,\<burstMaxExposureTime\>,\<burstEnableISOControl\>,\<burstOrder\>

| Field | Value | Description |
|:--|:--|:--|
| burstCaptureNum | int | Number of shots for burst shooting<br>1, 3, 5, 7, 9 |
| burstBracketStep | double | Bracket value range between each shot for burst shooting<br>0.0, 0.3, 0.7, 1.0, 1.3, 1.7, 2.0, 2.3, 2.7, 3.0 |
| burstCompensation | double | Exposure compensation for the base image and entire shooting for burst shooting<br>-5.0, -4.7, -4,3, -4.0, -3.7, -3,3, -3.0, -2.7, -2,3, -2.0, -1.7, -1,3, -1.0, -0.7, -0,3, 0.0, 0.3, 0.7, 1.0, 1.3, 1.7, 2.0, 2.3, 2.7, 3.0, 3.3, 3.7, 4.0, 4.3, 4.7, 5.0 |
| burstMaxExposureTime | double | Maximum exposure time for burst shooting<br>0.5, 0.625, 0.76923076, 1, 1.3, 1.6, 2, 2.5, 3.2, 4, 5, 6, 8, 10, 13, 15, 20, 25, 30, 40, 50, 60 |
| burstEnableISOControl | int | Adjustment with ISO sensitivity for burst shooting<br>0: Do not adjust with ISO sensitivity, 1: Adjust with ISO sensitivity |
| burstOrder | int | Shooting order for burst shooting<br>0: '0'→'-'→'+', 1: '-'→'0'→'+' |
