# 0xD802 AutoPowerOffDelay

**Vendor Extension Property**  
Returns and sets the current setting of the auto power off transition time (minutes).  

### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) | ![SC](https://img.shields.io/badge/SC-orange) | ![S](https://img.shields.io/badge/S-red) |
|:-:|:-:|:-:|:-:|:-:|
|   |   |   | ✓ | ✓ |

Refer to [`0xD81B AutoPowerOffDelaySec`](./auto_power_off_delay_sec.md) for THETA X/Z1/V.  

| Field Order | Field Name | Size | Data Type | Description |
|:-:|:--|:-:|:--|:--|
| 1 | Property Code | 2 | UINT16 | `0xD802` |
| 2 | Datatype | 2 | UINT16 | `0x0002` (UINT8) |
| 3 | Get/Set | 1 | UINT8 | `0x01` (GET/SET) |
| 4 | Default Value | 1 | UINT8 | `10` |
| 5 | Current Value | 1 | UINT8 ||
| 6 | Form Flag | 1 | UINT8 | `0x01` (Range) |
| 7 | Minimum Value | 1 | UINT8 | `0` (OFF) |
| 8 | Maximum Value | 1 | UINT8 | `30` (30 minutes) |
| 9 | Step Size | 1 | UINT8 | `1` (1 minute) |
