# sleepDelay

### Overview

Length of standby time before the camera enters the sleep mode.

Can be acquired by [camera.getOptions](../commands/camera.get_options.md) and set by [camera.setOptions](../commands/camera.set_options.md).

### Support model

| X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|
| All | All | All | All | All |

### Support value

#### For RICOH THETA V and later

60 to 65534, or 65535 (to disable the sleep mode).

If a value from "0" to "59" is specified, and error ([invalidParameterValue](../protocols/errors.md)) is returned.

#### For RICOH THETA S or SC

30 to 1800, or 65535 (to disable the sleep mode)
