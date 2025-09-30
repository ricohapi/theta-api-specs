# \_filter

### Overview

Image processing filter.

Configured the filter will be applied while in still image shooting mode. However, it is disabled during interval shooting, interval composite group shooting, multi bracket shooting or continuous shooting.

When \_filter is enabled, it takes priority over the exposure program ([exposureProgram](exposure_program.md)). Also, when \_filter is enabled, the exposure program is set to the Normal program.

The condition below will result in an error.

- When attempting to set `_filter` to `Noise reduction`, `HDR` or `Handheld HDR` while `fileFormat` is set to `raw+`, but this restriction is only for RICOH THETA Z1 firmware v1.80.1 or earlier.  
- [\_shootingMethod](_shooting_method.md) is except for Normal shooting and \_filter is enabled
- Access during video capture mode

The current setting can be acquired by [camera.getOptions](../commands/camera.get_options.md), and it can be changed by [camera.setOptions](../commands/camera.set_options.md).

### Support model

| X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|
| All | All | All | All | All |

### Support value

| Value | Description |
|:--|:--|
| off | No filter |
| DR Comp | DR compensation(RICOH THETA X is not supported) |
| Noise Reduction | Noise reduction |
| hdr | HDR<br>If you use shooting command ([camera.takePicture](../commands/camera.take_picture.md)) continuously while using HDR filter, the next shooting command cannot be used until the previous<br>shooting command is completed (i.e. state of [Commands/Status](../protocols/commands_status.md) is "done"). |
| Hh hdr | Handheld HDR<br>If you use shooting command ([camera.takePicture](../commands/camera.take_picture.md)) continuously while using HDR filter, the next shooting command cannot be used until the previous<br>shooting command is completed (i.e. state of [Commands/Status](../protocols/commands_status.md) is "done").<br>(RICOH THETA Z1 firmware v1.20.1 and later, RICOH THETA V firmware v3.10.1 and later, or RICOH THETA X firmware v2.40.0 and later.) |
