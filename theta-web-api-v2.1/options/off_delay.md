# offDelay

### Overview

Length of standby time before the camera automatically powers OFF.

Can be acquired by [camera.getOptions](../commands/camera.get_options.md) and set by [camera.setOptions](../commands/camera.set_options.md).

### Support model

| X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|
| All | All | All | All | All |

### Support value

#### For RICOH THETA V or later

0, or a value that is a multiple of 60 out of 600 or more and 2592000 or less (unit: second), or 65535.  
Return 0 when 65535 is set and obtained (Do not turn power OFF).

#### For RICOH THETA S or SC

30 or more and 1800 or less (unit: seconds), 65535 (Do not turn power OFF).
