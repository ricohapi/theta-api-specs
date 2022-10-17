# 0x99A7 ConvertVideoFormats

### Operation Code

0x99A7

### Overview

Converts the movie format of a saved movie.  
(Vendor Extension Operations)

Operation parameters are as follows.

| No. | Operation Parameter | RICOH THETA Specification |
|:--|:--|:--|
| 1 | VideoHandle | Video handle to be converted |
| 2 | Reserved | unused<br>Specify 0x00000000 |
| 3 | Reserved | unused<br>Specify 0x00000000 |
| 4 | Reserved | unused<br>Specify 0x00000000 |
| 5 | Reserved | unused<br>Specify 0x00000000 |

### Support model

| X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|
| All | v1.31.1 or later | v3.21.1 or later | --- | --- |

### Support value

The video formats information format is predetermined by the following.

#### RICOH THETA X

\<Size\>

<table>
    <thead>
      <tr>
        <th width="27%">Name</th>
        <th width="5%">Size</th>
        <th width="15%">Data Type</th>
        <th width="53%">Description</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>Size</td>
        <td>1</td>
        <td>UINT8</td>
        <td>Recorded size (1: 3840x1920)</td>
      </tr>
    </tbody>
  </table> 

#### RICOH THETA Z1 or prior

\<Size\>\<ProjectionType\>\<Codec\>\<TopBottomCorrection\>

<table>
    <thead>
      <tr>
        <th width="27%">Name</th>
        <th width="5%">Size</th>
        <th width="15%">Data Type</th>
        <th width="53%">Description</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>Size</td>
        <td>1</td>
        <td>UINT8</td>
        <td>Recorded size (0: 1920x960, 1: 3840x1920)</td>
      </tr>
      <tr>
        <td>ProjectionType</td>
        <td>1</td>
        <td>UINT8</td>
        <td>0: Equirectangular</td>
      </tr>
      <tr>
        <td>Codec</td>
        <td>1</td>
        <td>UINT8</td>
        <td>0: H.264/MPEG-4 AVC</td>
      </tr>
      <tr>
        <td>TopBottomCorrection</td>
        <td>1</td>
        <td>UINT8</td>
        <td>0: Apply, 1: ApplyFixedDirection, 2: Disapply</td>
      </tr>
    </tbody>
  </table> 
