# previewFormat

### Overview

Format of live view ([camera.getLivePreview](../commands/camera.get_live_preview.md)).

Can be acquired by [camera.getOptions](../commands/camera.get_options.md) and set by [camera.setOptions](../commands/camera.set_options.md).

### Support model

| X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|
| All | All | All | All | All |

### Support value

#### For RICOH THETA X

{"width": 3840, "height": 1920, "framerate": 30} \*1  
{"width": 1920, "height": 960, "framerate": 30} \*2  
{"width": 1024, "height": 512, "framerate": 30}  
{"width": 512, "height": 512, "framerate": 30}  

\*1 Recommend to use Ethernet to transfer 4K livePreview because wireless LAN may not have enough bandwidth for it.  
\*2 firmware v2.71.1 and later

#### For RICOH THETA V or Z1

{"width": 1920, "height": 960, "framerate": 8} \*2  
{"width": 1024, "height": 512, "framerate": 30} \*3  
{"width": 1024, "height": 512, "framerate": 8}  
{"width": 640, "height": 320, "framerate": 30} \*3  
{"width": 640, "height": 320, "framerate": 8} \*2  

\*2 firmware v1.00.1 and firmware v1.10.1 and later  
\*3 firmware v2.21.1 and later  

#### For RICOH THETA S or SC

{"width": 640, "height": 320, "framerate": 10}  
