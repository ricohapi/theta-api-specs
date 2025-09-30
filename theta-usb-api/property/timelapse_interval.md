# 0x501B TimelapseInterval

Sets and Returns the current value of the interval (msec) of shots in interval shooting mode.  

### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) | ![SC](https://img.shields.io/badge/SC-orange) | ![S](https://img.shields.io/badge/S-red) |
|:-:|:-:|:-:|:-:|:-:|
| ✓ | ✓ | ✓ | ✓ | ✓ |

| Field Order | Field Name | Size | Data Type | Description |
|:-:|:--|:-:|:--|:--|
| 1 | Property Code | 2 | UINT16 | `0x501B` |
| 2 | Datatype | 2 | UINT16 | `0x0006` (UINT32) |
| 3 | Get/Set | 1 | UINT8 | `0x01` (GET/SET) |
| 4 | Default Value | 4 | UINT32 | Refer to [Supported Value](#supported-values) |
| 5 | Current Value | 4 | UINT32 ||
| 6 | Form Flag | 1 | UINT8 | `0x01` (Range) |
| 7 | Minimum Value | 4 | UINT32 | Refer to [Supported Value](#supported-values) |
| 8 | Maximum Value | 4 | UINT32 | Refer to [Supported Value](#supported-values) |
| 9 | Step Size | 4 | UINT32 | `1000` (1000 msec) |

> [!WARNING]
> For THETA S/SC, this property is available only when [`0x5013 StillCaptureMode`](./still_capture_mode.md) 
 is `0x0001` Single-shot shooting. Configure this property prior to changing [`0x5013 StillCaptureMode`](still_capture_mode.md) to `0x0003` Interval shooting.  

### Supported Values

#### THETA X

| Field Name | Description |
|:--|:--|
| Default Value | `6000` (6 sec) |
| Minimum Value | `6000` (6 sec) |
| Maximum Value | `3600000` (3600 sec) |

#### THETA Z1

| [`0xD827 ImageFormat`](./image_format.md) | Field Name | Description |
|:--|:--|:--|
| `0x00` (JPEG) | Default Value | `6000` (6 sec) |
|               | Minimum Value | `6000` (6 sec) |
|               | Maximum Value | `3600000` (3600 sec) |
| `0x01` (RAW+) | Default Value | `10000` (10 sec) |
|               | Minimum Value | `10000` (10 sec) |
|               | Maximum Value | `3600000` (3600 sec) |

#### THETA V

| Field Name | Description |
|:--|:--|
| Default Value | `4000` (4 sec) |
| Minimum Value | `6000` (6 sec) |
| Maximum Value | `3600000` (3600 sec) |

#### THETA SC/S

| [`0x5003 ImageSize`](./image_size.md) | Field Name | Description |
|:--|:--|:--|
| `5376x2688\0` | Default Value | `8000` (8 sec) |
|               | Minimum Value | `8000` (8 sec) |
|               | Maximum Value | `3600000` (3600 sec) |
| `2048x1024\0` | Default Value | `5000` (5 sec) |
|               | Minimum Value | `5000` (5 sec) |
|               | Maximum Value | `3600000` (3600 sec) |
