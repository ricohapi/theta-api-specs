# dateTimeZone

### Overview

Current system time of RICOH THETA. Setting another options will result in an error.

The current setting can be acquired by [camera.getOptions](../commands/camera.get_options.md), and it can be changed by [camera.setOptions](../commands/camera.set_options.md).

With RICOH THETA X [camera.setOptions](../commands/camera.set_options.md) can be changed only when Date/time setting is AUTO in menu UI.

### Support model

| X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|
| All | All | All | All | All |

### Time format

YYYY:MM:DD hh:mm:ss+(-)hh:mm  
hh is in 24-hour time, +(-)hh:mm is the time zone.   
e.g. 2014:05:18 01:04:29+08:00
