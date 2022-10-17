# \_imageStitching

### Overview

Still image stitching setting during shooting.

Can be acquired by [camera.getOptions](../commands/camera.get_options.md) and set by [camera.setOptions](../commands/camera.set_options.md).

### Support model

| X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|
| All | All | v3.00.1 or later | --- | --- |

### Support value

| Key | Description |
|:--|:--|
| auto | Refer to stitching when shooting with "auto" |
| static | Performs static stitching |
| dynamic | Performs dynamic stitching(RICOH THETA X or later) |
| dynamicAuto | For Normal shooting, performs dynamic stitching, for Interval shooting, saves dynamic distortion correction parameters for the first image and then uses them for the 2nd and subsequent images(RICOH THETA X is not supported) |
| dynamicSemiAuto | Performs semi-dynamic stitching<br>Saves dynamic distortion correction parameters for the first image and then uses them for the 2nd and subsequent images(RICOH THETA X or later) |
| dynamicSave | Performs dynamic stitching and then saves distortion correction parameters |
| dynamicLoad | Performs stitching using the saved distortion correction parameters |
| none | Does not perform stitching |

For "none", captured still images are saved in a Dual-Fisheye format. For other than "none", captured still images are saved in an Equirectangular format.  

#### Restrictions based on the shooting method

| Model | Shooting method | Description |
|:--|:--|:--|
| V, Z1 | Multi-bracketing shooting<br>Interval composite shooting<br>Time shift shooting | Shoots with "auto" regardless of the specified Key |

#### Stitching when shooting with "auto"
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
        <td rowspan="3">V, Z1</td>
        <td>Normal shooting<br>Move interval shooting<br>Interval composite shooting<br>Time shift shooting</td>
        <td>Performs dynamic stitching</td>
      </tr>
      <tr>
        <td>Interval shooting<br>Fixed interval shooting</td>
        <td>Performs static stitching</td>
      </tr>
      <tr>
        <td>Multi-bracketing shooting</td>
        <td>Performs semi-dynamic stitching</td>
      </tr>
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
  