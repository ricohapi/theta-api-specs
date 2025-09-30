# 0xD823 MaxRecordableTime

**Vendor Extension Property**  
Returns or sets the current setting of the maximum recording time (seconds) per video.  

### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) | ![SC](https://img.shields.io/badge/SC-orange) | ![S](https://img.shields.io/badge/S-red) |
|:-:|:-:|:-:|:-:|:-:|
| ✓ | ✓ | ✓ |   |   |

| Field Order | Field Name | Size | Data Type | Description |
|:-:|:--|:-:|:--|:--|
| 1 | Property Code | 2 | UINT16 | `0xD823` |
| 2 | Datatype | 1 | UINT8 | `0x0004` (UINT16) |
| 3 | Get/Set | 1 | UINT8 | `0x01` (GET/SET) |
| 4 | Default Value | 2 | UINT16 | `300` (5 minutes) |
| 5 | Current Value | 2 | UINT16 ||
| 6 | Form Flag | 1 | UINT8 | `0x02` (Enumeration) |

### Supported Values

#### THETA X

`300`, `1500`, `7200`<sup>\*1</sup>  
<sup>\*1</sup>THETA X firmware v2.00.0 and later, only for 5.7K 2/5/10fps, 8K 2/5/10fps, and 2.7K\*2.7K 2/5/10fps mode.  
If you set 7200 seconds in 8K 10fps mode and then set back to 4K 30fps mode, the max recordable time will be overwritten to 1500 seconds automatically.  

#### THETA Z1

`300`, `1500`, `3000`<sup>\*2</sup>  
<sup>\*2</sup>THETA Z1 firmware v3.01.1 and later, only for 3.6K 1/2fps and 2.7K 1/2fps mode.  
If you set 3000 seconds in 3.6K 2fps mode and then set back to 4K 30fps mode, the max recordable time will be overwritten to 300 seconds automatically.  

#### THETA V

`300`, `1500`  
