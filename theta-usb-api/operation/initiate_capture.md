# 0x100E InitiateCapture

Starts shooting.  
If [`0x5012 CaptureDelay`](../property/capture_delay.md) is enabled, shooting will begin after the specified self-timer delay.  

> [!NOTE]
> If the InitiateCapture operation is requested under any of the following conditions, a DeviceBusy response will be returned during processing:  
> * While video recording or saving is in progress
> * When the [`0x5013 StillCaptureMode`](../property/still_capture_mode.md) is set to a mode other than single shot

### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) | ![SC](https://img.shields.io/badge/SC-orange) | ![S](https://img.shields.io/badge/S-red) |
|:-:|:-:|:-:|:-:|:-:|
| ✓ | ✓ | ✓ | ✓ | ✓ |

| | |
|:--|:--|
| Operation Code | `0x100E` |
| Operation Parameter 1 | `StorageID`<sup>\*1</sup> |
| Operation Parameter 2 | `ObjectFormatCode`<sup>\*1</sup> |
| Operation Parameter 3 | None |
| Operation Parameter 4 | None |
| Operation Parameter 5 | None |
| Data | None |
| Data Direction | N/A |

<sup>\*1</sup>Unused. Specify `0x00000000`.  
