# 0x5003 ImageSize

### Device Prop Code

0x5003

### Overview

Acquires or sets the recorded size (pixels).

### Support model

| X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|
| All | All | All | All | All |

### Support value

#### For RICOH THETA X

<table border="0">
  <thead>
    <tr>
      <th style="text-align: left">Shooting mode</th>
      <th style="text-align: left">Value</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td rowspan="2">Still image shooting mode</td>
      <td>"11008×5504"</td>
    </tr>
    <tr>
      <td>"5504×2752"</td>
    </tr>
    <tr>
      <td rowspan="5">Movie shooting mode</td>
      <td>"7680x3840"</td>
    </tr>
    <tr>
      <td>"5760x2880"</td>
    </tr>
    <tr>
      <td>"3840x1920"</td>
    </tr>
    <tr>
      <td>"1920x960"</td>
    </tr>
    <tr>
      <td>"2752x2752" *1</td>
    </tr>
  </tbody>
</table>

\*1 RICOH THETA X firmware v2.50.2 or later. This mode outputs two fisheye video for each lens. The MP4 file name ending with `_0` is the video file on the front lens, and `_1` is back lens.  

#### For RICOH THETA Z1

<table border="0">
  <thead>
    <tr>
      <th style="text-align: left">Shooting mode</th>
      <th style="text-align: left">Value</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td rowspan="1">Still image shooting mode</td>
      <td>"6720x3360"</td>
    </tr>
    <tr>
      <td rowspan="4">Movie shooting mode</td>
      <td>"3840x1920"</td>
    </tr>
    <tr>
      <td>"1920x960"</td>
    </tr>
    <tr>
      <td>"3648x3648" *2</td>
    </tr>
    <tr>
      <td>"2688x2688" *2</td>
    </tr>
  </tbody>
</table>

\*2 RICOH THETA Z1 firmware v3.01.1 or later. This mode outputs two fisheye video for each lens. The MP4 file name ending with `_0` is the video file on the front lens, and `_1` is back lens. This mode does not record audio track to MP4 file.  

#### For RICOH THETA V

<table border="0">
  <thead>
    <tr>
      <th style="text-align: left">Shooting mode</th>
      <th style="text-align: left">Value</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td rowspan="1">Still image shooting mode</td>
      <td>"5376x2688"</td>
    </tr>
    <tr>
      <td rowspan="2">Movie shooting mode</td>
      <td>"3840x1920"</td>
    </tr>
    <tr>
      <td>"1920x960"</td>
    </tr>
  </tbody>
</table>

#### For RICOH THETA S or SC

<table border="0">
  <thead>
    <tr>
      <th style="text-align: left">Shooting mode</th>
      <th style="text-align: left">Value</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td rowspan="2">Still image shooting mode</td>
      <td>"5376x2688"</td>
    </tr>
    <tr>
      <td>"2048x1024"</td>
    </tr>
    <tr>
      <td rowspan="2">Movie shooting mode</td>
      <td>"1920x1080"</td>
    </tr>
    <tr>
      <td>"1280x720"</td>
    </tr>
  </tbody>
</table>

### Event

Since the value of FreeSpaceInImages of [StorageInfo](../operation/get_storage_info.md) changes when ImageSize has been changed, a [StorageInfoChanged](../event/storage_info_changed.md) event is informed.
