# Shutter Speed

### Service

1D0F3602-8DFB-4340-9045-513040DAD991

### Characteristic

D3CE2AED-10FA-4648-833D-CD74C6F35905

### Format

sint8

### Overview

Acquires and sets the shutter speed setting of the camera.

It can be set for video shooting mode at RICOH THETA V firmware v3.00.1 and later. Shooting settings are retained separately for both the Still image shooting mode and Video shooting mode.

### Value Fields

The choise is listed below. There are certain range difference between each models and settings.

<table border="0" style="width: 70%;">
  <thead>
    <tr>
      <th style="text-align: left"><a href="capture_mode.md">Capture Mode</a></th>
      <th style="text-align: left"><a href="exposure_program.md">Exposure Program</a></th>
      <th style="text-align: left">V and later</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td rowspan="2">Still image shooting mode</td>
      <td>Manual</td>
      <td>1/25000 to 60</td>
    </tr>
    <tr>
      <td>Shutter priority</td>
      <td>1/25000 to 1/8<br>1/25000 to 15 <span class="mintext">*2</span></td>
    </tr>
    <tr>
      <td>Video shooting mode <span class="mintext">*1</span></td>
      <td>Manual or Shutter priority</td>
      <td class="description_item">1/25000 to 1/30</td>
    </tr>
    <tr>
      <td colspan="2">Otherwise</td>
      <td class="description_item">0 (AUTO)</td>
    </tr>
  </tbody>
</table>

\*1 RICOH THETA V firmware v3.00.1 and later  
\*2 RICOH THETA Z1 firmware v1.50.1 and later and RICOH THETA V firmware v3.40.1 and later

#### Supported value

| Value | Description |
|:--|:--|
| 0 | AUTO |
| 1 | 1/25000 |
| 2 | 1/20000 |
| 3 | 1/16000 |
| 4 | 1/12500 |
| 5 | 1/10000 |
| 6 | 1/8000 |
| 7 | 1/6400 |
| 8 | 1/5000 |
| 9 | 1/4000 |
| 10 | 1/3200 |
| 11 | 1/2500 |
| 12 | 1/2000 |
| 13 | 1/1600 |
| 14 | 1/1250 |
| 15 | 1/1000 |
| 16 | 1/800 |
| 17 | 1/640 |
| 18 | 1/500 |
| 19 | 1/400 |
| 20 | 1/320 |
| 21 | 1/250 |
| 22 | 1/200 |
| 23 | 1/160 |
| 24 | 1/125 |
| 25 | 1/100 |
| 26 | 1/80 |
| 27 | 1/60 |
| 28 | 1/50 |
| 29 | 1/40 |
| 30 | 1/30 |
| 31 | 1/25 |
| 32 | 1/20 |
| 33 | 1/15 |
| 34 | 1/13 |
| 35 | 1/10 |
| 36 | 1/8 |
| 37 | 1/6 |
| 38 | 1/5 |
| 39 | 1/4 |
| 40 | 1/3 |
| 41 | 1/2.5 |
| 42 | 1/2 |
| 43 | 1/1.6 |
| 44 | 1/1.3 |
| 45 | 1 |
| 46 | 1.3 |
| 47 | 1.6 |
| 48 | 2 |
| 49 | 2.5 |
| 50 | 3.2 |
| 51 | 4 |
| 52 | 5 |
| 53 | 6 |
| 54 | 8 |
| 55 | 10 |
| 56 | 13 |
| 57 | 15 |
| 58 | 20 |
| 59 | 25 |
| 60 | 30 |
| 61 | 60 |
| 62 | 40\*3 |
| 63 | 50\*3 |

\*3 RICOH THETA Z1 firmware v2.10.1 and later and RICOH THETA V firmware v3.80.1 and later.  

### Properties

| Property | Requirement |
|:--|:--|
| Read | Mandatory |
| Write | Mandatory |
| Notify | Excluded |
