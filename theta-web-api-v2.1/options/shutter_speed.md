# shutterSpeed

### Overview

Shutter speed (sec).

It can be set for video shooting mode at RICOH THETA V firmware v3.00.1 and later. Shooting settings are retained separately for both the Still image shooting mode and Video shooting mode.

Can be acquired by [camera.getOptions](../commands/camera.get_options.md) and set by [camera.setOptions](../commands/camera.set_options.md).

### Support model

| X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|
| All | All | All | All | All |

### Support value

The choise is listed below. There are certain range difference between each models and settings.

<table border="0">
  <thead>
    <tr>
      <th style="text-align: left"><a href="capture_mode.md">captureMode</a></th><th><a href="exposure_program.md">exposureProgram</a></th>
      <th style="text-align: left">X and later</th>
      <th style="text-align: left">V or Z1</th>
      <th class="description_item">SC</th>
      <th style="text-align: left">S</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td rowspan="2">Still image shooting mode</td>
      <td>Manual</td>
      <td>0.0000625 (1/16000) to 60</td>
      <td>0.00004 (1/25000) to 60</td>
      <td>0.000125 (1/8000) to 60</td>
      <td>0.00015625 (1/6400) to 60</td>
    </tr>
    <tr>
      <td>Shutter priority</td>
      <td>0.0000625 (1/16000) to 15</td>
      <td>0.00004 (1/25000) to 0.125 (1/8)<br>0.00004 (1/25000) to 15 <span class="mintext">*2</span></td>
      <td>0.000125 (1/8000) to 0.125 (1/8)</td>
      <td>0.00015625 (1/6400) to 0.125 (1/8)</td>
    </tr>
    <tr>
      <td>Video shooting mode <span class="mintext">*1</span></td>
      <td>Manual or Shutter priority</td>
      <td>0.0000625 (1/16000) to 0.03333333 (1/30)</td>
      <td>0.00004 (1/25000) to 0.03333333 (1/30)</td>
      <td>--</td>
      <td>--</td>
    </tr>
    <tr>
      <td colspan="2">Otherwise</td>
      <td colspan="4" class="description_item">0 (AUTO)</td>
    </tr>
  </tbody>
</table>

\*1 RICOH THETA Z1 and RICOH THETA V firmware v3.00.1 and later  
\*2 RICOH THETA Z1 firmware v1.50.1 and later and RICOH THETA V firmware v3.40.1 and later

#### Support value

0.00004 (1/25000), 0.00005 (1/20000), 0.0000625 (1/16000), 0.00007812(1/12800)\*3,  
0.00008 (1/12500)\*4, 0.0001 (1/10000), 0.000125 (1/8000),  
0.00015625 (1/6400), 0.0002 (1/5000), 0.00025 (1/4000),  
0.0003125 (1/3200), 0.0004 (1/2500), 0.0005 (1/2000),  
0.000625 (1/1600), 0.0008 (1/1250), 0.001 (1/1000),  
0.00125 (1/800), 0.0015625 (1/640), 0.002 (1/500),  
0.0025 (1/400), 0.003125 (1/320), 0.004 (1/250),  
0.005 (1/200), 0.00625 (1/160), 0.008 (1/125),  
0.01 (1/100), 0.0125 (1/80), 0.01666666 (1/60),  
0.02 (1/50), 0.025 (1/40), 0.03333333 (1/30),  
0.04 (1/25), 0.05 (1/20), 0.06666666 (1/15),  
0.07692307 (1/13), 0.1 (1/10), 0.125 (1/8),  
0.16666666 (1/6), 0.2 (1/5), 0.25 (1/4),  
0.33333333 (1/3), 0.4 (1/2.5), 0.5 (1/2),  
0.625 (1/1.6), 0.76923076 (1/1.3), 1,  
1.3, 1.6, 2, 2.5, 3.2, 4, 5,  
6, 8, 10, 13, 15, 20, 25, 30, 40\*5, 50\*5, 60

\*3 Enabled only for RICOH THETA X.  
\*4 No support for RICOH THETA X.  
\*5 RICOH THETA Z1 firmware v2.10.1 and later and RICOH THETA V firmware v3.80.1 and later. For RICOH THETA X, all versions are supported.  
