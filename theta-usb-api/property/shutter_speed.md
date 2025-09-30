# 0xD00F ShutterSpeed

**Vendor Extention Property**  
Returns and Sets the current setting of the shutter speed (seconds).  
This setting is available in video recording mode on RICOH THETA V firmware v3.00.1 and later. Shooting settings are maintained separately for still capture mode and video recording mode.  

### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) | ![SC](https://img.shields.io/badge/SC-orange) | ![S](https://img.shields.io/badge/S-red) |
|:-:|:-:|:-:|:-:|:-:|
| ✓ | ✓ | ✓ | ✓ | ✓ |

| Field Order | Field Name | Size | Data Type | Description |
|:-:|:--|:-:|:--|:--|
| 1 | Property Code | 2 | UINT16 | `0xD00F` |
| 2 | Datatype | 2 | UINT16 | `0x0008` (UINT64) |
| 3 | Get/Set | 1 | UINT8 | `0x01` (GET/SET) |
| 4 | Default Value | 8 | UINT64 | `0x0000` ||
| 5 | Current Value | 8 | UINT64 ||
| 6 | Form Flag | 1 | UINT8 | `0x02` (Enumeration) |

### Supported Values

The following values are supported when the exposure program ([`0x500E ExposureProgramMode`](./exposure_program_mode.md)) is set to `0x0002` Manual or `0x0004` Shutter Priority.  

> [!NOTE]
> To specify a value of `1/100`, set `1` in the upper 4 bytes and `100` in the lower 4 bytes of the UINT64.
This format follows the RATIONAL type as defined in TIFF.  

`1,25000` (1/25000 sec)<sup>\*1</sup>,  
`1,20000` (1/20000 sec), `1,16000` (1/16000 sec), `1,12500` (1/12500 sec)<sup>\*1</sup>, `1,12800` (1/12800 sec),  
`1,10000` (1/10000 sec), `1,8000` (1/8000 sec),`1,6400` (1/6400 sec), `1,5000` (1/5000 sec), `1,4000` (1/4000 sec),  
`1,3200` (1/3200 sec), `1,2500` (1/2500 sec), `1,2000` (1/2000 sec), `1,1600` (1/1600 sec), `1,1250` (1/1250 sec),  
`1,1000` (1/1000 sec), `1,800` (1/800 sec), `1,640` (1/640 sec), `1,500` (1/500 sec), `1,400` (1/400 sec),  
`1,320` (1/320 sec), `1,250` (1/250 sec), `1,200` (1/200 sec), `1,160` (1/160 sec), `1,125` (1/125 sec),  
`1,100` (1/100 sec), `1,80` (1/80 sec), `1,60` (1/60 sec), `1,50` (1/50 sec), `1,40` (1/40 sec),  
`1,30` (1/30 sec), `1,25` (1/25 sec), `1,20` (1/20 sec), `1,15` (1/15 sec), `1,13` (1/13 sec),  
`1,10` (1/10 sec), `1,8` (1/8 sec), `1,6` (1/6 sec), `1,5` (1/5 sec), `1,4` (1/4 sec),  
`1,3` (1/3 sec), `10,25` (1/2.5 sec), `1,2` (1/2 sec), `10,16` (1/1.6 sec), `10,13` (1/1.3 sec),  
`1,1` (1 sec), `13,10` (1.3 sec), `16,10` (1.6 sec), `2,1` (2 sec), `25,10` (2.5 sec),  
`32,10` (3 sec), `4,1` (4 sec), `5,1` (5 sec), `6,1` (6 sec), `8,1` (8 sec),  
`10,1` (10 sec), `13,1` (13 sec), `15,1` (15 sec), `20,1` (20 sec), `25,1` (25 sec),  
`30,1` (30 sec), `40,1` (40 sec)<sup>\*2\*3</sup>, `50,1` (50 sec)<sup>\*2\*3</sup>, `60,1` (60 sec),  
`0,0` (Automatic)  

<sup>\*1</sup>Available only for THETA Z1/V  
<sup>\*2</sup>For THETA Z1, available with firmware v2.10.1 and later  
<sup>\*3</sup>For THETA V, available with firmware v3.80.1 and later  

#### THETA X

| Shooting mode | ExposureProgramMode | Supported Range |
|:--|:--|:--|
| Still capture mode   | Manual           | 1/16000 sec to 60 sec |
|                      | Shutter priority | 1/16000 sec to 15 sec |
| Video recording mode | Manual           | 1/16000 sec to 1/30 sec |
|                      | Shutter priority | 1/16000 sec to 1/30 sec |
| Otherwise            | --               | `0` (Automatic) |

#### THETA Z1/V

| Shooting mode | ExposureProgramMode | Supported Range |
|:--|:--|:--|
| Still capture mode   | Manual           | 1/25000 sec to 60 sec |
|                      | Shutter priority | 1/25000 sec to 1/8 sec<br>1/25000 sec to 15 sec<sup>\*4\*5</sup> |
| Video recording mode | Manual           | 1/25000 sec to 1/30 sec<sup>\*6</sup> |
|                      | Shutter priority | 1/25000 sec to 1/30 sec<sup>\*6</sup> |
| Otherwise            | --               | `0` (Automatic) |

<sup>\*4</sup>For THETA Z1, change the spec with firmware v1.50.1 and later  
<sup>\*5</sup>For THETA V, change the spec with firmware v3.40.1 and later  
<sup>\*6</sup>For THETA V, available with firmware v3.00.1 and later  

#### THETA SC

| Shooting mode | ExposureProgramMode | Supported Range |
|:--|:--|:--|
| Still capture mode   | Manual           | 1/8000 sec to 60 sec |
|                      | Shutter priority | 1/8000 sec to 1/8 sec |
| Video recording mode | Manual           | -- (Not supported) |
|                      | Shutter priority | -- (Not supported) |
| Otherwise            | --               | `0` (Automatic) |

#### THETA S

| Shooting mode | ExposureProgramMode | Supported Range |
|:--|:--|:--|
| Still capture mode   | Manual           | 1/6400 sec to 60 sec |
|                      | Shutter priority | 1/6400 sec to 1/8 sec |
| Video recording mode | Manual           | -- (Not supported) |
|                      | Shutter priority | -- (Not supported) |
| Otherwise            | --               | `0` (Automatic) |
