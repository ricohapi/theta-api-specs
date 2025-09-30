# 0x5013 StillCaptureMode

Returns and sets the current setting of the shooting method.  

### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) | ![SC](https://img.shields.io/badge/SC-orange) | ![S](https://img.shields.io/badge/S-red) |
|:-:|:-:|:-:|:-:|:-:|
| ✓ | ✓ | ✓ | ✓ | ✓ |

| Field Order | Field Name | Size | Data Type | Description |
|:-:|:--|:-:|:--|:--|
| 1 | Property Code | 2 | UINT16 | `0x5013` |
| 2 | Datatype | 2 | UINT16 | `0x0004` (UINT16) |
| 3 | Get/Set | 1 | UINT8 | `0x01` (GET/SET) |
| 4 | Default Value | 2 | UINT16 | `0x0001` |
| 5 | Current Value | 2 | UINT16 ||
| 6 | Form Flag | 1 | UINT8 | `0x02` (Enumeration) |

### Supported Values

| Value | ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) | ![SC](https://img.shields.io/badge/SC-orange) | ![S](https://img.shields.io/badge/S-red) | Description |
|:-:|:-:|:-:|:-:|:-:|:-:|:--|
| `0x0001` | ✓ | ✓ | ✓ | ✓ | ✓ | Single-shot shooting<sup>\*1</sup> |
| `0x0003` | ✓ | ✓ | ✓ | ✓ | ✓ | Interval shooting<sup>\*1</sup> |
| `0x8002` | ✓ | ✓ | ✓ | ✓ | ✓ | **Video Recording mode** |
| `0x8003` |   | ✓ |   | ✓<sup>\*2</sup> | ✓<sup>\*3</sup> | Interval Composite shooting<sup>\*1</sup> |
| `0x8004` | ✓ | ✓ | ✓ | ✓<sup>\*2</sup> | ✓<sup>\*3</sup> | Multi Bracket shooting<sup>\*1</sup> |
| `0x8005` | ✓ | ✓ | ✓ |   | ✓ | **Live Streaming mode** |
| `0x8006` | ✓ | ✓<sup>\*5</sup> | ✓<sup>\*6</sup> |   |   | Continious shooting<sup>\*1</sup> for THETA X<br>Interval shooting<sup>\*1</sup> Tripod stabilization: OFF for THETA Z1/V |
| `0x8007` | ✓ | ✓<sup>\*5</sup>  | ✓<sup>\*6</sup> |   |   | Time Shift shooting<sup>\*1</sup> for THETA X<br>Interval shooting<sup>\*1</sup> Tripod stabilization: ON for THETA Z1/V |
| `0x8008` |   | ✓<sup>\*7</sup> |   |   |   | Burst shooting<sup>\*1</sup> |

<sup>\*1</sup>Available only for Still Capture mode  
<sup>\*2</sup>THETA SC firmware v1.10 and later  
<sup>\*3</sup>THETA S firmware v1.82 and later  
<sup>\*4</sup>THETA V firmware v3.00.1 and later  
<sup>\*5</sup>THETA Z1 firmware v1.50.1 and later  
<sup>\*6</sup>THETA V firmware v3.40.1 and later  
<sup>\*7</sup>THETA Z1 firmware v2.10.1 and later  

### Event

A [`0x4006 DevicePropChanged`](../event/device_prop_changed.md) event is issued when the shooting mode is changed through camera operation.  
