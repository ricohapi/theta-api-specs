# captureInterval

### Overview

Shooting interval (sec.) for interval shooting.

The current setting can be acquired by [camera.getOptions](../commands/camera.get_options.md), and it can be changed by [camera.setOptions](../commands/camera.set_options.md).

### Support model

| X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|
| All | All | All | All | All |

### Support value

The value that can be set differs depending on the image format ([fileFormat](file_format.md)) to be shot.

#### For RICOH THETA X or later

<table>
  <thead>
  <tr>
    <th>Image format</th>
    <th>Image size</th>
    <th>Support value</th>
  </tr>
  </thead>
  <tbody>
  <tr>
    <td>JPEG</td>
    <td>11008 x 5504<br>5504 x 2752</td>
    <td>Minimum value (minInterval): 6<br>Maximum value (maxInterval): 3600</td>
  </tr>
  </tbody>
</table>

#### For RICOH THETA Z1

<table>
  <thead>
  <tr>
    <th>Image format</th>
    <th>Image size</th>
    <th>Support value</th>
  </tr>
  </thead>
  <tbody>
  <tr>
    <td>JPEG</td>
    <td>6720 x 3360</td>
    <td>Minimum value (minInterval): 6<br>Maximum value (maxInterval): 3600</td>
  </tr>
  <tr>
    <td>RAW+</td>
    <td>6720 x 3360</td>
    <td>Minimum value (minInterval): 10<br>Maximum value (maxInterval): 3600</td>
  </tr>
  </tbody>
</table>

#### For RICOH THETA V

<table>
  <thead>
  <tr>
    <th>Image format</th>
    <th>Image size</th>
    <th>Support value</th>
  </tr>
  </thead>
  <tbody>
  <tr>
    <td>JPEG</td>
    <td>5376 x 2688</td>
    <td>Minimum value (minInterval): 4<br>Maximum value (maxInterval): 3600</td>
  </tr>
  </tbody>
</table>

#### For RICOH THETA S or SC

<table>
  <thead>
  <tr>
    <th>Image format</th>
    <th>Image size</th>
    <th>Support value</th>
  </tr>
  </thead>
  <tbody>
  <tr>
    <td rowspan="2">JPEG</td>
    <td>5376 x 2688</td>
    <td>Minimum value (minInterval): 8<br>Maximum value (maxInterval): 3600</td>
  </tr>
  <tr>
    <td>2048 x 1024</td>
    <td>Minimum value (minInterval): 5<br>Maximum value (maxInterval): 3600</td>
  </tr>
  </tbody>
</table>
