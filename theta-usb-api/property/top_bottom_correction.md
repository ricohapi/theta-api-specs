# 0xD825 TopBottomCorrection

**Vendor Extension Property**  
Returns or sets the current setting of top/bottom correction (zenith correction).  
For THETA Z1/V, this property can be used only for still capture mode.  
For THETA X, this property can also be applied to video recording mode.  

### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) | ![SC](https://img.shields.io/badge/SC-orange) | ![S](https://img.shields.io/badge/S-red) |
|:-:|:-:|:-:|:-:|:-:|
| ✓ | ✓ | ✓<sup>\*1</sup> |   |   |

<sup>\*1</sup>THETA V firmware v3.00.1 and later  

| Field Order | Field Name | Size | Data Type | Description |
|:-:|:--|:-:|:--|:--|
| 1 | Property Code | 2 | UINT16 | `0xD825` |
| 2 | Datatype | 1 | UINT8 | `0x0002` (UINT8) |
| 3 | Get/Set | 1 | UINT8 | `0x01` (GET/SET) |
| 4 | Default Value | 1 | UINT8 | `0x00` |
| 5 | Current Value | 1 | UINT8 ||
| 6 | Form Flag | 1 | UINT8 | `0x02` (Enumeration) |

### Supported Values

| Value | Description |
|:--|:--|
| `0x00` | `Apply` Performs top/bottom correction (zenith correction) |
| `0x01` | `ApplyAuto` Refer to [ApplyAuto](#applyauto) section |
| `0x02` | `ApplySave` Performs top/bottom correction and saves the zenith parameters |
| `0x03` | `ApplyLoad` Performs top/bottom correction using the saved zenith parameters |
| `0x04` | `Disapply` Not performs top/bottom correction  |
| `0x05` | `ApplySemiAuto`<sup>\*1</sup>The first shot operates with `ApplySave`, and the second and subsequent shots operate with `ApplyLoad`. |

<sup>\*1</sup>Supported by only THETA X  

> [!NOTE]  
> For THETA Z1/V,  
> `Apply` is always executed regardless of the setting in Interval Shooting (tripod stabilization: OFF), Interval Composite Shooting, and Time-shift Shooting modes.  
> `ApplyAuto` is always executed regardless of the setting in Interval shooting (tripod stabilization: ON) and Multi bracketing shooting modes.  

### ApplyAuto

#### THETA X

| Shooting Method | Description |
|:--|:--|
| Multi bracketing shooting | `ApplySemiAuto` is executed |
| Otherwise | `Apply` is executed |

#### THETA Z1/V

| Shooting Method | Description |
|:--|:--|
| Interval shooting<br>Interval shooting (tripod stabilization: ON)<br>Multi bracketing shooting | Same behavior as `ApplySemiAuto` |
| Otherwise | `Apply` is executed |
