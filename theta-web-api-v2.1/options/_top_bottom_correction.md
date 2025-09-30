# \_topBottomCorrection

### Overview

Sets the top/bottom correction.  
For RICOH THETA V and RICOH THETA Z1, the top/bottom correction can be set only for still images.  
For RICOH THETA X, the top/bottom correction can be set for both still images and videos.  

Can be acquired by [camera.getOptions](../commands/camera.get_options.md) and set by [camera.setOptions](../commands/camera.set_options.md).

### Support model

| X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|
| All | All | v3.00.1 and later | --- | --- |

### Support value

| Key | Description |
|:--|:--|
| Apply | Top/bottom correction is performed. |
| ApplyAuto | Refer to top/bottom correction when shooting with "ApplyAuto" |
| ApplySemiAuto | Top/bottom correction is performed. The parameters used for top/bottom correction for the first image are saved and used for the 2nd and subsequent images.(RICOH THETA X and later) |
| ApplySave | Performs top/bottom correction and then saves the parameters. |
| ApplyLoad | Performs top/bottom correction using the saved parameters. |
| Disapply | Does not perform top/bottom correction. |
| Manual\*1 | Performs the top/bottom correction with the specified front position. The front position can be specified with [_topBottomCorrectionRotation](../options/_top_bottom_correction_rotation.md). |

\*1 RICOH THETA X firmware v1.20.0 and later

#### Restrictions based on the shooting method

<table>
    <thead>
      <tr>
        <th>Model</th>
        <th>Shooting method</th>
        <th>Description</th>
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

#### Top/bottom correction when shooting with "ApplyAuto"
<table>
    <thead>
      <tr>
        <th>Model</th>
        <th>Shooting method</th>
        <th>Description</th>
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
