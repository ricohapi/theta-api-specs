# 0xD834 ImageStitching

**Vendor Extension Property**  
Returns or sets the current setting of stitching for still capture mode.  

### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) | ![SC](https://img.shields.io/badge/SC-orange) | ![S](https://img.shields.io/badge/S-red) |
|:-:|:-:|:-:|:-:|:-:|
| ✓ | ✓<sup>\*1</sup> |   |   |   |

<sup>\*1</sup>THETA Z1 v2.10.1 and later  

| Field Order | Field Name | Size | Data Type | Description |
|:-:|:--|:-:|:--|:--|
| 1 | Property Code | 2 | UINT16 | `0xD834` |
| 2 | Datatype | 1 | UINT8 | `0x0004` (UINT16) |
| 3 | Get/Set | 1 | UINT8 | `0x01` (GET/SET) |
| 4 | Default Value | 2 | UINT16 | `0x0001` (Auto) |
| 5 | Current Value | 2 | UINT16 ||
| 6 | Form Flag | 1 | UINT8 | `0x02` (Enumeration) |

### Supported Values

| Value | Description |
|:--|:--|
| `0x0001` | `auto` Performs stitching. Refer to [Auto](#auto) section |
| `0x0002` | `none` Not performs stitching |
| `0x0003` | `static` Performs static stitching |
| `0x0004` | `dynamic` Performs dynamic stitching |
| `0x0005` | `dynamicSemiAuto`<sup>\*2</sup> The first shot operates with `dynamicSave`, and the second and subsequent shots operate with `dynamicLoad`. |
| `0x0006` | `dynamicSave` Performs dynamic stitching and saves the stitching parameters |
| `0x0007` | `dynamicLoad` Performs dynamic stitching using the saved stitching parameters |

<sup>\*2</sup>Supported by only THETA X  

### auto

#### THETA X

| Shooting Method | Description |
|:--|:--|
| Multi bracketing shooting | `dynamicSemiAuto` is executed |
| Otherwise | `dynamic` is executed |

#### THETA Z1

| Shooting Method | Description |
|:--|:--|
| Interval shooting mode | `static` is executed |
| Interval shooting (tripod stabilization: ON) | Same behavior as `dynamicSemiAuto` |
| Otherwise | `dynamic` is executed |
