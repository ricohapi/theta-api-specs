# 0xD825 TopBottomCorrection

### Device Prop Code

0xD825

### Overview

Acquires and sets the top/bottom correction setting for still image.  
On the RICOH THETA X, this can also be applied to video.  
(Vendor Extension Property)

### Support model

| X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|
| All | All | v3.00.1 or later | --- | --- |

### Support value

| Value | Description |
|:--|:--|
| 0x00 | Top/bottom correction is performed. |
| 0x01 | Refer to top/bottom correction when shooting with "0x01" |
| 0x02 | Performs top/bottom correction and then saves the parameters. |
| 0x03 | Performs top/bottom correction using the saved parameters. |
| 0x04 | Does not perform top/bottom correction. |
| 0x05 | Top/bottom correction is performed. The parameters used for top/bottom correction for the first image are saved and used for the 2nd and subsequent images. (RICOH THETA X or later) |

#### Restrictions based on the shooting method

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
        <td rowspan="2">V, Z1</td>
        <td>Move interval shooting<br>Interval composite shooting<br>Time shift shooting</td>
        <td>Shoots with "Apply" regardless of the specified Key</td>
      </tr>
      <tr>
        <td>Fixed interval shooting<br>Multi-bracketing shooting</td>
        <td>Shoots with "ApplyAuto" regardless of the specified Key</td>
      </tr>
    </tbody>
  </table>  

#### Top/bottom correction when shooting with "0x01"
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
        <td rowspan="2">V, Z1</td>
        <td>Interval shooting<br>Fixed interval shooting<br>Multi-bracketing shooting</td>
        <td>The parameters used for top/bottom correction for the first image are saved and used for the 2nd and subsequent images.</td>
      </tr>
      <tr>
        <td>Normal shooting</td>
        <td>Top/bottom correction is performed.</td>
      </tr>
      <tr>
        <td rowspan="2">X</td>
        <td>Multi-bracketing shooting</td>
        <td>The parameters used for top/bottom correction for the first image are saved and used for the 2nd and subsequent images.</td>
      </tr>
      <tr>
        <td>Except for Multi-bracketing shooting</td>
        <td>Top/bottom correction is performed.</td>
      </tr>
    </tbody>
  </table>  
