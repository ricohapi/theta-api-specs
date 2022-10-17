# 0xD00F ShutterSpeed

### Device Prop Code

0xD00F

### Overview

Acquires or sets the shutter speed (sec).   
(Vendor Extension Property)

It can be set for video shooting mode at RICOH THETA V firmware v3.00.1 or later. Shooting settings are retained separately for both the Still image shooting mode and Video shooting mode.

### Support model

| X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|
| All | All | All | All | All |

### Support value

Similar to the RATIONAL type of the Exif2.3 standard.   
For example, "1/8000" is expressed as "1, 8000".

The choise is listed below. There are certain range difference between each models and settings.

<table border="0">
  <thead>
    <tr>
      <th style="text-align: left">Shooting mode</th>
      <th style="text-align: left"><a href="exposure_program_mode.md">ExposureProgramMode</a></th>
      <th style="text-align: left">X or later</th>
      <th style="text-align: left">V or later</th>
      <th style="text-align: left">SC</th>
      <th style="text-align: left">S</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td rowspan="2">Still image shooting mode</td>
      <td>Manual</td>
      <td>1/16000 to 60</td>
      <td>1/25000 to 60</td>
      <td>1/8000 to 60</td>
      <td>1/6400 to 60</td>
    </tr>
    <tr>
      <td>Shutter priority</td>
      <td>1/16000 to 15</td>
      <td>1/25000 to 1/8<br>1/25000 to 15 <span class="mintext">*2</span></td>
      <td>1/8000 to 1/8</td>
      <td>1/6400 to 1/8</td>
    </tr>
    <tr>
      <td>Video shooting mode <span class="mintext">*1</span></td>
      <td>Manual or Shutter priority</td>
      <td>1/16000 to 1/30</td>
      <td>1/25000 to 1/30</td>
      <td>--</td>
      <td>--</td>
    </tr>
    <tr>
      <td colspan="2">Otherwise</td>
      <td colspan="3">0 (AUTO)</td>
    </tr>
  </tbody>
</table>

\*1 RICOH THETA Z1 and RICOH THETA V firmware v3.00.1 or later  
\*2 RICOH THETA Z1 firmware v1.50.1 or later and RICOH THETA V firmware v3.40.1 or later

#### Support value

1/25000, 1/20000, 1/16000, 1/12800 \*3, 1/12500 \*4, 1/10000, 1/8000,  
 1/6400, 1/5000, 1/4000, 1/3200, 1/2500,  
 1/2000, 1/1600, 1/1250, 1/1000, 1/800,  
 1/640, 1/500, 1/400, 1/320, 1/250,  
 1/200, 1/160, 1/125, 1/100, 1/80,  
 1/60, 1/50, 1/40, 1/30, 1/25,  
 1/20, 1/15, 1/13, 1/10, 1/8,  
 1/6, 1/5, 1/4, 1/3, 10/25,  
 1/2, 10/16, 10/13, 1, 13/10,  
 16/10, 2/1, 25/10, 32/10, 4/1,  
5/1, 6/1, 8/1, 10/1, 13/1,  
 15/1, 20/1, 25/1, 30/1, 40/1 \*5, 50/1 \*5, 60/1,  
0 (AUTO, setting is not available)

\*3 Enabled only for RICOH THETA X.  
\*4 No support for RICOH THETA X.  
\*5 RICOH THETA Z1 firmware v2.10.1 or later and RICOH THETA V firmware v3.80.1 or later. For RICOH THETA X, all versions are supported.  
