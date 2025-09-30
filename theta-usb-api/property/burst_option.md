# 0xD839 BurstOption

**Vendor Extension Property**  
Returns or sets the current settings of Burst shooting mode.  

### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) | ![SC](https://img.shields.io/badge/SC-orange) | ![S](https://img.shields.io/badge/S-red) |
|:-:|:-:|:-:|:-:|:-:|
|   | ✓<sup>\*1</sup> |   |   |   |

<sup>\*1</sup>THETA X firmware v2.10.1 and later

| Field Order | Field Name | Size | Data Type | Description |
|:-:|:--|:-:|:--|:--|
| 1 | Property Code | 2 | UINT16 | `0xD839` |
| 2 | Datatype | 2 | UINT16 | `0xFFFF` (STRING) |
| 3 | Get/Set | 1 | UINT8 | `0x01` (GET/SET) |
| 4 | Default Value | 1 | STRING | `/0` |
| 5 | Current Value | 60 | STRING ||
| 6 | Form Flag | 1 | UINT8 | `0x00` (None) |

### Format of Current Value

`burstCaptureNum`,`burstBracketStep`,`burstCompensation`,`burstMaxExposureTime`,`burstEnableISOControl`,`burstOrder`  

| Field Name | Value | Description |
|:--|:--|:--|
| `burstCaptureNum` | `1`, `3`, `5`, `7`, `9` | Number of burst capture frames |
| `burstBracketStep` | `0.0`,<br>`0.3`, `0.7`, `1.0`,<br>`1.3`, `1.7`, `2.0`,<br>`2.3`, `2.7`, `3.0` | Bracket step (Ev) of burst capture mode |
| `burstCompensation` | `-5.0`, `-4.7`, `-4,3`,<br>`-4.0`, `-3.7`, `-3,3`,<br>`-3.0`, `-2.7`, `-2,3`,<br>`-2.0`, `-1.7`, `-1,3`,<br>`-1.0`, `-0.7`, `-0,3`,<br>`0.0`,<br>`0.3`, `0.7`, `1.0`,<br>`1.3`, `1.7`, `2.0`,<br>`2.3`, `2.7`, `3.0`,<br>`3.3`, `3.7`, `4.0`,<br>`4.3,` `4.7`, `5.0` | Exposure compensation of burst capture mode|
| `burstMaxExposureTime` | `0.5`, `0.625`, `0.76923076`,<br>`1`, `1.3`, `1.6`, `2`, `2.5`, `3.2`,<br>`4`, `5`, `6`, `8`, `10`, `13`,<br>`15`, `20`, `25`, `30`, `40`, `50`, `60` | The maximum exposure time (seconds) of burst capture mode |
| `burstEnableISOControl` | `0`, `1` | Auto ISO control of burst capture mode<br>`0`: Disable auto ISO control. This means to set always ISO80 when auto exposure mode<br>`1`: Enable auto ISO control. This means to allow higher ISO sensitivity |
| `burstOrder` | `0`, `1` | Shooting order of exposure setting<br>`0`: `0` > `-` > `+`<br>`1` : `-`→`0`→`+` |
