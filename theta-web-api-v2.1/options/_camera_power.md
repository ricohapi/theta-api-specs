# \_cameraPower

### Overview

`_cameraPower` is the power status of camera.  
Can be acquired by [camera.getOptions](../commands/camera.get_options.md) and set by [camera.setOptions](../commands/camera.set_options.md).

### Support model

| X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|
| v2.61.0 and later | -- | -- | -- | -- |

### Support value

| Name | Description |
|:--|:--|
| `off` | Power off |
| `on`  | Power on  |
| `powerSaving` | Power on, power saving mode. Camera is closed. \*1 |
| `silentMode`  | Power on, silent mode. LCD/LED is turned off. \*1  |

\*1 : Unavailable parameter when plugin is running. In this case, `invalidParameterValue` error will be returned.  
