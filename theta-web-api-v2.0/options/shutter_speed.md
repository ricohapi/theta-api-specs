# shutterSpeed

### Overview

Shutter speed (sec.).

The current setting can be acquired by [camera.getOptions](../commands/camera.get_options.md), and it can be changed by [camera.setOptions](../commands/camera.set_options.md).

### Support value

0.000125(1/8000) (RICOH THETA SC only),  
0.00015625(1/6400), 0.0002(1/5000), 0.00025(1/4000),  
 0.0003125(1/3200), 0.0004(1/2500), 0.0005(1/2000),  
 0.000625(1/1600), 0.0008(1/1250), 0.001(1/1000),  
 0.00125(1/800), 0.0015625(1/640), 0.002(1/500),  
 0.0025(1/400), 0.003125(1/320), 0.004(1/250),  
 0.005(1/200), 0.00625(1/160), 0.008(1/125),  
 0.01(1/100), 0.0125(1/80), 0.01666666(1/60),  
 0.02(1/50), 0.025(1/40), 0.03333333(1/30),  
 0.04(1/25), 0.05(1/20), 0.06666666(1/15),  
 0.07692307(1/13), 0.1(1/10), 0.125(1/8),  
 0.16666666(1/6), 0.2(1/5), 0.25(1/4),  
 0.33333333(1/3), 0.4(1/2.5), 0.5(1/2),  
 0.625(1/1.6), 0.76923076(1/1.3), 1,  
 1.3, 1.6, 2, 2.5, 3.2, 4, 5,  
 6, 8, 10, 13, 15, 20, 25, 30, 60

However, from 1/6 sec to 60 sec can only be set when the exposure program ([exposureProgram](exposure_program.md)) is manual.

0 when the shutter speed is AUTO. Settings cannot be configured.
