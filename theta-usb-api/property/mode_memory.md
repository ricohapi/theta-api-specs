# 0xD841 ModeMemory

**Vendor Extension Property**  
Mode Memory has been introduced to retain some settings instead of reverting to defaults, when the device enters sleep mode or is powered off.  

### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) | ![SC](https://img.shields.io/badge/SC-orange) | ![S](https://img.shields.io/badge/S-red) |
|:-:|:-:|:-:|:-:|:-:|
|   | ✓<sup>\*1</sup> |   |   |   |

<sup>\*1</sup>THETA Z1 firmware v3.60.3 and later

| Field Order | Field Name | Size | Data Type | Description |
|:-:|:--|:-:|:--|:--|
| 1 | Property Code | 2 | UINT16 | `0xD841` |
| 2 | Datatype | 2 | UINT16 | `0x0002` (UINT8) |
| 3 | Get/Set | 1 | UINT8 | `0x01` (GET/SET) |
| 4 | Default Value | 1 | UINT8 | `0` |
| 5 | Current Value | 1 | UINT8 ||
| 6 | Form Flag | 1 | UINT8 | `0x02` (None) |

| Value | Description |
|:-:|:--|
| `0` | When the device enters sleep mode or is powered off,<br>the following settings **will revert to their default values**. |
| `1` | When the device enters sleep mode or is powered off,<br>the following settings **will be retained for the next startup**.  |

- Still image stitching process
- Exposure program / Aperture / Shutter speed / ISO sensitivity / Exposure compensation
- White balance mode / Color temperature setting
- Filters
- Interval shooting: number of shots / interval
- Multi-bracket shooting: number of shots / parameters
- Interval composite shooting: duration / intermediate saving
- Time-shift shooting settings (excluding shooting order)
- Burst shooting options
- Geotag data

> [!NOTE]  
> THETA X and A1 always retain these settings.  
