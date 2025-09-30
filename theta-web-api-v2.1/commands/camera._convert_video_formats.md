# camera.\_convertVideoFormats

### Overview

Converts the movie format of a saved movie.

### Support model

| X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|
| All | All | All | --- | --- |

### Parameters

<table>
  <thead>
    <tr>
      <th style="text-align: left">Name</th>
      <th style="text-align: left">Type</th>
      <th style="text-align: left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>fileUrl</td>
      <td>String</td>
      <td>URL of a saved movie file</td>
    </tr>
    <tr>
      <td>size</td>
      <td>String</td>
      <td>Recorded size (pixels)<br />Z1, V: Specify "3840 x 1920" or "1920 x 960".<br />X: Specify "3840 x 1920".</td>
    </tr>
    <tr>
      <td>projectionType</td>
      <td>String</td>
      <td>Projection type of movie file<br />Specify "Equirectangular" .<br />RICOH THETA X is not supported.</td>
    </tr>
    <tr>
      <td>codec</td>
      <td>String</td>
      <td>Codec<br />Specify "H.264/MPEG-4 AVC".<br />RICOH THETA X is not supported.</td>
    </tr>
    <tr>
      <td>topBottomCorrection</td>
      <td>String</td>
      <td>Top/bottom correction
      <table>
        <thead>
          <tr>
            <th style="text-align: left">Value</th>
            <th style="text-align: left">Description</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>"Apply"</td>
            <td>Top/bottom correction enabled<br /> and rotational shake correction<span class="mintext">*</span> enabled.</td>
          </tr>
          <tr>
            <td>"ApplyFixedDirection"<span class="mintext">*</span></td>
            <td>Both top/bottom correction and rotational shake perfect correction enabled.</td>
          </tr>
          <tr>
            <td>"Disapply"</td>
            <td>Top/bottom correction disabled.</td>
          </tr>
        </tbody>
      </table>
      <span class="mintext">*</span> Rotational shake correction and rotational shake perfect correction are supported from RICOH THETA V firmware v1.20.1 and later.<br /><br />RICOH THETA X is not supported.</td>
    </tr>
  </tbody>
</table>

### Progress

| Name | Type | Description |
|:--|:--|:--|
| completion | Number | Progress of movie file conversion |

### Results

| Name | Type | Description |
|:--|:--|:--|
| fileUrl | String | URL of a converted movie file |

### Example

#### Parameters

```
{
    "fileUrl":"http://192.168.1.1/files/abcde/100RICOH/R0010017.mp4",
    "size":"3840x1920",
    "projectionType":"Equirectangular",
    "codec":"H.264/MPEG-4 AVC",
    "topBottomCorrection":"Apply"
}
```

#### Progress

```
{
    "completion": 0.1
}
```

#### Results

```
{
    "fileUrl":"http://192.168.1.1/files/abcde/100RICOH/R0010017.mp4"
}
```
