# \_filter

### Overview

Image processing filter.

Configured the filter will be applied while in still image shooting mode. However, it is disabled during continuous shooting.

When \_filter is enabled, it takes priority over the exposure program ([exposureProgram](exposure_program.md)). Also, when \_filter is enabled, the exposure program is set to the Normal program.

The current setting can be acquired by [camera.getOptions](../commands/camera.get_options.md), and it can be changed by [camera.setOptions](../commands/camera.set_options.md).

### Support value

| Value | Description |
|:--|:--|
| off | No filter |
| DR Comp | DR compensation |
| Noise Reduction | Noise reduction |
| hdr | HDR (RICOH THETA S firmware 01.21 or later)<br>If you use shooting command ([camera.takePicture](../commands/camera.take_picture.md)) continuously while using<br>HDR filter, the next shooting command cannot be used until the previous<br>shooting command is completed (i.e. state of [Commands/Status](../protocols/commands_status.md) is "done"). |
