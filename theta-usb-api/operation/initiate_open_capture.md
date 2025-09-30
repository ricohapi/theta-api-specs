# 0x101C InitiateOpenCapture

Starts continuous shooting.  

* In image capturing mode, starts interval shooting, interval composite shooting, multi-bracket shooting, time-shift shooting, burst shooting, or continuous shooting.
* In video recording mode, starts video recording.

Refer to [`0x5013 StillCaptureMode`](../property/still_capture_mode.md) for shooting mode.  
If [`0x5012 CaptureDelay`](../property/capture_delay.md) is enabled, starts self-timer shooting.  

### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) | ![SC](https://img.shields.io/badge/SC-orange) | ![S](https://img.shields.io/badge/S-red) |
|:-:|:-:|:-:|:-:|:-:|
| ✓ | ✓ | ✓ | ✓ | ✓ |

| | |
|:--|:--|
| Operation Code | `0x101C` |
| Operation Parameter 1 | `StorageID`<sup>\*1</sup> |
| Operation Parameter 2 | `ObjectFormatCode`<sup>\*1</sup> |
| Operation Parameter 3 | None |
| Operation Parameter 4 | None |
| Operation Parameter 5 | None |
| Data | None |
| Data Direction | N\A |

<sup>\*1</sup>Unused. Specify `0x00000000`.
