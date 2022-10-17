# 0xD80B Filter

### Device Prop Code

0xD80B

### Overview

Acquire or set the image processing filter.  
(Vendor Extension Property)

The set filter is applied to the still image shooting mode.  
It is disabled when interval shooting, interval composite shooting, multi bracket shooting or continuous shooting starts.

When filter is enabled, it takes priority over the exposure program ([ExposureProgramMode](exposure_program_mode.md)). Also, when \_filter is enabled, the exposure program is set to normal program.

The condition below will result in an error.

- [ImageFormat](image_format.md) is RAW+ and Filter is Noise reduction, HDR or Handheld HDR
- Registers shooting conditions in My Settings is except for Normal shooting and Filter is enabled (RICOH THETA Z1)
- Access duaring video capture mode

### Support model

| X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|
| All | All | All | All | All |

### Support value

| Value | Description |
|:--|:--|
| 0x00 | No filter |
| 0x01 | DR compensation \*2 |
| 0x02 | Noise reduction |
| 0x03 | HDR |
| 0x04 | Handheld HDR \*1\*2\*3 |

 \*1 RICOH THETA Z1 firmware v1.20.1 or later and RICOH THETA V firmware v3.10.1 or later  

 \*2 RICOH THETA X is not supported
 
 \*3 RICOH THETA SC, S is not supported
