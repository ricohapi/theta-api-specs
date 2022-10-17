# _burstOption

### Overview
Burst shooting setting.

Can be acquired by [camera.getOptions](../commands/camera.get_options.md) and set by [camera.setOptions](../commands/camera.set_options.md).

### Support model

| X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|
| --- | v2.10.1 or later | --- | --- | --- |

### Support value

| Value | Description |
|:--|:--|
| _burstCaptureNum | Number of shots for burst shooting<br>1, 3, 5, 7, 9 |
| _burstBracketStep | Bracket value range between each shot for burst shooting<br>0.0, 0.3, 0.7, 1.0, 1.3, 1.7, 2.0, 2.3, 2.7, 3.0 |
| _burstCompensation | Exposure compensation for the base image and entire shooting for burst shooting<br>-5.0, -4.7, -4,3, -4.0, -3.7, -3,3, -3.0, -2.7, -2,3, -2.0, -1.7, -1,3, -1.0, -0.7, -0,3, 0.0, 0.3, 0.7, 1.0, 1.3, 1.7, 2.0, 2.3, 2.7, 3.0, 3.3, 3.7, 4.0, 4.3, 4.7, 5.0 |
| _burstMaxExposureTime | Maximum exposure time for burst shooting<br>0.5, 0.625, 0.76923076, 1, 1.3, 1.6, 2, 2.5, 3.2, 4, 5, 6, 8, 10, 13, 15, 20, 25, 30, 40, 50, 60 |
| _burstEnableIsoControl | Adjustment with ISO sensitivity for burst shooting<br>0: Do not adjust with ISO sensitivity, 1: Adjust with ISO sensitivity |
| _burstOrder | Shooting order for burst shooting<br>0: '0' → '-' → '+', 1: '-' → '0' → '+' |

### Example

#### Options

```
{
    "_burstOption": {
        "_burstCaptureNum":9,
        "_burstBracketStep":0.0,
        "_burstCompensation":0.0,
        "_burstMaxExposureTime":15,
        "_burstEnableIsoControl":0,
        "_burstOrder":0
    }
}
```