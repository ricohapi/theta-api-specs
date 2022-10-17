# Date Time Zone

### Service

32886D39-BA23-425C-BCAE-9C1DB0066922

### Characteristic

5D485AC4-FF08-40C9-B920-8FC20196E40C

### Overview

Acquires and sets the time of the internal clock of the camera.

### Value Fields

| Name | Type | Description |
|:--|:--|:--|
| Year | sint16 | 2017 -- 2034 |
| Month | sint8 | 1 -- 12 |
| Day | sint8 | 1 -- 31 |
| Hours | sint8 | 0 -- 23 |
| Minutes | sint8 | 0 -- 59 |
| Seconds | sint8 | 0 -- 59 |
| Time Zone | utf8 | + (-) hh:mm (Fixed to 6 digits) |

### Properties

| Property | Requirement |
|:--|:--|
| Read | Mandatory |
| Write | Mandatory |
| Notify | Excluded |
