# 0xD006 ErrorInfo

**Vendor Extension Property**  
Returns error information.  

### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) | ![SC](https://img.shields.io/badge/SC-orange) | ![S](https://img.shields.io/badge/S-red) |
|:-:|:-:|:-:|:-:|:-:|
| ✓ | ✓ | ✓ | ✓ | ✓ |

| Field Order | Field Name | Size | Data Type | Description |
|:-:|:--|:-:|:--|:--|
| 1 | Property Code | 2 | UINT16 | `0xD006` |
| 2 | Datatype | 2 | UINT16 | `0x0006` (UINT32) |
| 3 | Get/Set | 1 | UINT8 | `0x00` (GET) |
| 4 | Default Value | 4 | UINT32 | `0` |
| 5 | Current Value | 4 | UINT32 ||
| 6 | Form Flag | 1 | UINT8 | `0x00` (None) |

### Supported Values

#### THETA X

| Value | Error Code | Shootable<br>State | Description | Recommended Action |
|:-:|:--|:-:|:--|:--|
| `0x00000001` | Insufficient memory || Occurs when the shutter release button is pressed while the remaining shot count is 0. | Delete unnecessary files |
| `0x00000004` | Excessive file number || Occurs when the maximum file number is exceeded. Restored by resetting the file number. | Delete the "999" folder or remove 9999 files |
| `0x00000008` | Clock not set | ✓ | Occurs when the internal clock of the camera is not set. | Set the date and time via API, user interface, or NTP |
| `0x00000010`<sup>\*2</sup> | Electronic compass error | ✓ | Occurs when there is an error with the electronic compass. | Move the camera in a figure-eight (∞) pattern |
| `0x00000020` | Unsupported media type | ✓ | Occurs when an unsupported media type is used (e.g., SDHC). | Use a microSDXC card |
| `0x00000040` | Unsupported file system | ✓ | Occurs when an unsupported file system is detected (e.g., FAT32). | Format the microSD card |
| `0x00000100` | Media not ready | ✓ | Error while mounting the memory | Wait until the microSD card is mounted |
| `0x00000200` | Insufficient battery | ✓ | Low battery warning (e.g., during firmware update). | Charge the battery |
| `0x00000400` | Invalid file | ✓ | Firmware file mismatch | Retry the firmware update |
| `0x00000800` | Plugin boot error | ✓ | Plugin startup warning (IoT technical standards compliance). | Disconnect from the internet |
| `0x00001000` | In-progress error || Occurs when performing continuous shooting by camera operation while executing *Delete object*, *Transfer firmware file*, *Install plugin*, or *Uninstall plugin* via WebAPI or MTP. | Wait until processing is finished |
| `0x00001000` | Cannot record || Condition: Battery inserted + WLAN ON + Video mode + 4K 60fps / 5.7K 10fps / 5.7K 15fps / 5.7K 30fps / 8K 10fps. | Turn off WLAN |
| `0x00002000` | Cannot record due to low battery || Condition: Battery inserted + Battery level at or below threshold + WLAN ON + Video mode + 4K 30fps. | Charge the battery |
| `0x00400000` | Shooting hardware failure || Occurs when a failure is detected in shooting-related hardware. | Rebooting the camera may help |
| `0x00800000` | Software error || Software error | Rebooting the camera may help |
| `0x08000000` | Internal memory access error || Occurs when the internal memory of the camera cannot be accessed. | Rebooting the camera may help |
| `0x20000000` | Miscellaneous error || An error other than those listed above. | Rebooting the camera may help |
| `0x40000000` | Charging error || Occurs when a USB charging error is detected. The camera powers off when this error occurs. | Check the USB cable or charger |
| `0x00100000`<sup>\*1</sup> | Board temperature warning | ✓ | Occurs when the internal temperature of the camera approaches the upper limit. | Allow the camera to cool |
| `0x80000000` | Board temperature error || Occurs when the internal temperature of the camera exceeds the upper limit. The camera powers off when this error occurs. | Allow the camera to cool |
| `0x00200000` | Battery temperature error || Occurs when the battery temperature exceeds the upper limit. The camera powers off when this error occurs. | Allow the camera to cool |

<sup>\*1</sup>THETA X firmware v1.40.0 and later  
<sup>\*2</sup>THETA X firmware v2.40.0 and later  

#### THETA Z1 and earlier

| Value | Error Code | Shootable<br>State | Description | Recommended Action |
|:-:|:--|:-:|:--|:--|
| `0x00000001` | Insufficient memory || Occurs when the shutter release button is pressed while the remaining shot count is 0. | Delete unnecessary files |
| `0x00000004` | Excessive file number || Occurs when the maximum file number is exceeded.<br>Restored by resetting the file number. | Delete the "999" folder or 9999 files |
| `0x00000008` | Clock not set | ✓ | Occurs when the internal clock of the camera has not been set. | Set the date and time via API |
| `0x00000010` | Electronic compass error | ✓ | Occurs when an error is detected in the electronic compass. | Move the camera in a figure-eight (∞) pattern |
| `0x00000800`<sup>\*3</sup> | Plugin boot error | ✓ | Plugin startup warning (IoT technical standards compliance). | Disconnect from the internet |
| `0x00100000`<sup>\*4</sup> | Board temperature warning | ✓ | Occurs when the internal temperature of the camera approaches the upper limit. | Allow the camera to cool |
| `0x00400000` | Shooting hardware failure || Occurs when a failure is detected in shooting-related hardware. | Rebooting the camera may help |
| `0x08000000` | Internal memory access error || Occurs when the internal memory of the camera cannot be accessed. | Rebooting the camera may help |
| `0x20000000` | Miscellaneous error || An error other than those listed above. | Rebooting the camera may help |
| `0x40000000` | Charging error || Occurs when a USB charging error is detected. The camera powers off when this error occurs. | Check the USB cable or charger |
| `0x80000000` | Board temperature error || Occurs when the internal temperature of the camera exceeds the upper limit. The camera powers off when this error occurs. | Allow the camera to cool |
| `0x00200000`<sup>\*1</sup> | Battery temperature error || Occurs when the battery temperature exceeds the upper limit. The camera powers off when this error occurs. | Allow the camera to cool |

<sup>\*3</sup>Only for THETA Z1  
<sup>\*4</sup>THETA Z1 firmware v2.20.3 and later  
