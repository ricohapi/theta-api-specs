# Camera Error

### Service

9AD04FDF-E62B-43E4-8593-7631FCD29874

### Characteristic

C9434C4A-37DE-44D2-ACAF-19CC3E8E34E5

### Format

sint16

### Overview

Acquires error information.

### Value Fields

| Name | Type | Description |
|:--|:--|:--|
| Number of Camera Errors | sint8 | Number of camera errors. |

Returns for data in the following format for the number of camera errors.

| Name | Type | Description |
|:--|:--|:--|
| Camera Error | sint8 | camera error defined below. |

Errors in detail

| Value | Description |
|:--|:--|
| 0 | Insufficient memory<br>Issued when the shutter release button is pressed while the number of remaining available shots is "0". |
| 2 | Excessive file number<br>Issued when the maximum file number is exceeded. Restored by resetting the file number. |
| 3 | Clock unset<br>Issued when the internal clock of the camera is not set. |
| 4 | Electronic compass error<br>Issued when there is an error with the electronic compass. |
| 9 | Shooting hardware failure detection<br>Issued when a failure has been detected with hardware used for shooting. |
| 14 | Internal memory access error<br>Issued when the internal memory of the camera cannot be accessed. |
| 16 | Miscellaneous error |
| 17 | Charging error<br>Issued when the a USB charging error has been detected. The camera is powered off when this error occurs. |
| 18 | (Board) temperature error<br>Issued when the internal temperature of the camera is higher than the upper limit temperature. The camera is powered off when this error occurs. |
| 19 \*1 | Battery temperature error<br>Issued when the battery temperature of the camera is higher than the upper limit temperature. The camera is powered off when this error occurs. |
| 21 \*1 | Plugin boot error<br>Plugin start warning. (IoT technical standards compliance) |

\*1 RICOH THETA Z1 or later

### Properties

| Property | Requirement |
|:--|:--|
| Read | Mandatory |
| Write | Excluded |
| Notify | Mandatory |
