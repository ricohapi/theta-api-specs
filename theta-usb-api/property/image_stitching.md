# 0xD834 Image Stitching

### Device Prop Code

0xD834

### Overview

Still image stitching setting during shooting.  
(Vendor Extension Property)

### Support model

| X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|
| All | v2.10.1 or later | --- | --- | --- |

### Support value

| Value | Description |
|:--|:--|
| 0x0001 | Automatic<br>Refer to stitching when shooting with "0x0001" |
| 0x0002 | Does not perform stitching |
| 0x0003 | Performs static stitching |
| 0x0004 | Performs dynamic stitching |
| 0x0005 | (RICOH THETA X)<br>Performs semi-dynamic stitching<br>Saves dynamic distortion correction parameters for the first image and then uses them for the 2nd and subsequent images<br><br>(RICOH THETA Z1)<br>Reserved |
| 0x0006 | Performs dynamic stitching and then saves distortion correction parameters |
| 0x0007 | Performs stitching using the saved distortion correction parameters |

For "0x0002", captured still images are saved in a Dual-Fisheye format. For other than "0x0002", captured still images are saved in an Equirectangular format.  

#### Stitching when shooting with "0x0001"
<table>
    <thead>
      <tr>
        <th width="14%">Model</th>
        <th width="43%">Shooting method</th>
        <th width="43%">Description</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td rowspan="2">X</td>
        <td>Multi-bracketing shooting</td>
        <td>Performs semi-dynamic stitching</td>
      </tr>
      <tr>
        <td>Except for Multi-bracketing shooting</td>
        <td>Performs dynamic stitching</td>
      </tr>
    </tbody>
  </table>
