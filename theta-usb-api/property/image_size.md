# 0x5003 ImageSize

Returns and sets the current setting of image size.  

### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) | ![SC](https://img.shields.io/badge/SC-orange) | ![S](https://img.shields.io/badge/S-red) |
|:-:|:-:|:-:|:-:|:-:|
| ✓ | ✓ | ✓ | ✓ | ✓ |

| Field Order | Field Name | Size | Data Type | Description |
|:-:|:--|:-:|:--|:--|
| 1 | Property Code | 2 | UINT16 | `0x5003` |
| 2 | Datatype | 2 | UINT16 | `0xFFFF` (STRING) |
| 3 | Get/Set | 1 | UINT8 | `0x01` (GET/SET) |
| 4 | Default Value | Variable | STRING ||
| 5 | Current Value | Variable | STRING ||
| 6 | Form Flag | 1 | UINT8 | `0x02` (Enumeration) |

### Supported Values

#### THETA X

| Shooting Mode | Value |
|:--|:--|
| Still capture mode | `11008x5504\0` |
|                    | `5504x2752\0`  |
| Video recording mode | `7680x3840\0` |
|                      | `5760x2880\0` |
|                      | `3840x1920\0` |
|                      | `1920x960\0`  |
|                      | `2752x2752\0`<sup>\*1</sup> |

<sup>\*1</sup>THETA X firmware v2.50.2 and later. This mode outputs two fisheye video for each lens. The MP4 file name ending with `_0` is the video file on the front lens, and `_1` is back lens.  

#### THETA Z1

| Shooting Mode | Value |
|:--|:--|
| Still capture mode | `6720x3360\0` |
| Video recording mode | `3840x1920\0` |
|                      | `1920x960\0`  |
|                      | `3648x3648\0`<sup>\*2</sup> |
|                      | `2688x2688\0`<sup>\*2</sup> |

<sup>\*2</sup>THETA Z1 firmware v3.01.1 and later. This mode outputs two fisheye video for each lens. The MP4 file name ending with `_0` is the video file on the front lens, and `_1` is back lens. This mode does not record audio track to MP4 file.  

#### THETA V

| Shooting Mode | Value |
|:--|:--|
| Still capture mode | `5376x2688\0` |
| Video recording mode | `3840x1920\0` |
|                      | `1920x960\0`  |

#### THETA S/SC

| Shooting Mode | Value |
|:--|:--|
| Still capture mode | `5376x2688\0` |
|                    | `2048x1024\0` |
| Video recording mode | `1920x960\0` |
|                      | `1280x720\0` |

### Event

When [`0x5003 ImageSize`](./image_size.md) is changed, the `Free Space In Objects` value in [`0x1005 StorageInfo`](../operation/get_storage_info.md) is updated, and a [`0x400C StorageInfoChanged`](../event/storage_info_changed.md) event is notified.  
