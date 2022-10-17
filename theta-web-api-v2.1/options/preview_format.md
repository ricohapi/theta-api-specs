# previewFormat

### Overview

Format of live view ([camera.getLivePreview](../commands/camera.get_live_preview.md)).

Can be acquired by [camera.getOptions](../commands/camera.get_options.md) and set by [camera.setOptions](../commands/camera.set_options.md).

### Support model

| X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|
| All | All | All | All | All |

### Support value

#### For RICOH THETA X or later

{"width": 1024, "height": 512, "framerate": 30}

#### For RICOH THETA V or Z1

{"width": 1920, "height": 960, "framerate": 8} \*1

{"width": 1024, "height": 512, "framerate": 30} \*2

{"width": 1024, "height": 512, "framerate": 8}

{"width": 640, "height": 320, "framerate": 30} \*2

{"width": 640, "height": 320, "framerate": 8} \*1

\*1 firmware v1.00.1 and firmware v1.10.1 or later

\*2 firmware v2.21.1 or later

#### For RICOH THETA S or SC

{"width": 640, "height": 320, "framerate": 10}
