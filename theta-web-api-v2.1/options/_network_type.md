# \_networkType

### Overview

Network type.

Can be acquired by [camera.getOptions](../commands/camera.get_options.md) and set by [camera.setOptions](../commands/camera.set_options.md).

### Support model

| X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|
| All | All | All | --- | --- |

### Support value

#### RICOH THETA X

| Value | Description |
|:--|:--|
| OFF | Network is off. This value can be gotten only by plugin. (firmware v1.40.0 or later)|
| AP | Direct mode |
| CL | Client mode |

#### RICOH THETA V, Z1

| Value | Description |
|:--|:--|
| OFF | Network is off. This value can be gotten only by plugin.|
| AP | Direct mode |
| CL | Client mode via WLAN, see also [camera.\_setAccessPoint](../commands/camera._set_access_point.md). |
| ETHERNET | Client mode via Ethernet cable |
