# 0xD82C BluetoothRole

**Vendor Extension Property**  
Returns or sets the current setting of the Bluetooth role.  

### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) | ![SC](https://img.shields.io/badge/SC-orange) | ![S](https://img.shields.io/badge/S-red) |
|:-:|:-:|:-:|:-:|:-:|
|   | ✓<sup>\*1</sup> | ✓<sup>\*2</sup> |   |   |

<sup>\*1</sup>THETA Z1 firmware v1.31.1 and later  
<sup>\*2</sup>THETA V firmware v3.21.1 and later  

| Field Order | Field Name | Size | Data Type | Description |
|:-:|:--|:-:|:--|:--|
| 1 | Property Code | 2 | UINT16 | `0xD82C` |
| 2 | Datatype | 2 | UINT16 | `0x0002` (UINT8) |
| 3 | Get/Set | 1 | UINT8 | `0x01` (GET/SET) |
| 4 | Default Value | 1 | UINT8 | `0x02` |
| 5 | Current Value | 1 | UINT8 ||
| 6 | Form Flag | 1 | UINT8 | `0x02` (Enumeration) |

### Supported Values

| Value | Description |
|:-:|:--|
| `0x01` | **Central**: Enabled,  **Peripheral**: Disabled |
| `0x02` | **Central**: Disabled, **Peripheral**: Enabled |
| `0x03` | **Central**: Enabled,  **Peripheral**: Enabled |
