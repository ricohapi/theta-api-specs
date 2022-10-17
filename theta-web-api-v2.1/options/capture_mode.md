# captureMode

### Overview

Shooting mode.

The current setting can be acquired by [camera.getOptions](../commands/camera.get_options.md), and it can be changed by [camera.setOptions](../commands/camera.set_options.md).

Swithcing modes may take time. Wait a while to send the command that takes place after switching the mode.

Live streaming mode is supported by only RICOH THETA S.

### Support model

| X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|
| All | All | All | All | All |

### Support value (Still image capture mode or Video capture mode)

| Value | Description |
|:--|:--|
| image | Still image capture mode |
| video | Video capture mode |

Switching to Live streaming mode is not supported by API.

### Support value (Live streaming mode)

| Value | Description |
|:--|:--|
| _liveStreaming | Live streaming mode |

Switching to Still image capture mode or Video capture mode is not supported by API.
