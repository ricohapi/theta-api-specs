# 0xD006 ErrorInfo

### Device Prop Code

0xD006

### Overview

Acquire error information.   
(Vendor Expansion Properties)

### Warning code

| PropValue | Error Description | Details |
|:--|:--|:--|
| 0x00000001 | Insufficient memory space | Issued when the shutter button is pressed when the remaining number of photos is 0. |
| 0x00000004 | File number exceeded | Issued when the file number limitation is exceeded.<br>Recovered by resetting the file number. |
| 0x00000008 | Clock not set | Issued when the camera's internal clock is not set. |
| 0x00000010 | Electromagnetic compass error | Issued when an error occurs in the electromagnetic compass. |

### Error code

| PropValue | Error Description | Details |
|:--|:--|:--|
| 0x80000000 | Temperature error | Issued when the temperature detected inside the camera exceeds the standard temperature, and the camera power is simultaneously turned off. |
| 0x40000000 | Recharging Error | Issued when a USB recharging error is detected, and the camera power is simultaneously turned off. |
| 0x20000000 | Other errors | Other errors. |
| 0x10000000 | SD memory card access error | Issued when an error in which the SD memory card cannot be accessed is detected. |
| 0x08000000 | Internal memory access error | Issued when an error in which the camera internal memory cannot be accessed is detected. |
| 0x04000000 | SD memory card format error | Issued when an error in which the SD memory card is not initialized is detected. |
| 0x02000000 | Internal memory format error | Issued when an error in which the internal memory is not be initialized is detected. |
| 0x01000000 | SD memory card fault | Issued when a fault is detected in the SD memory card. |
| 0x00400000 | Shooting hardware error detected | Issued when a malfunction is detected in the hardware used for shooting. |
