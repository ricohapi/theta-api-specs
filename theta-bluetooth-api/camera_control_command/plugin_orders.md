# Plugin Orders

### Service

32886D39-BA23-425C-BCAE-9C1DB0066922

### Characteristic

8F710EDC-6F9B-45D4-A5F7-E6EDA304E790

### Overview

Acquires or sets the plugins for plugin mode.  
RICOH THETA Z1 and later.

### Value Fields

| Name | Type | Description |
|:--|:--|:--|
| 1st | sint8 | Plugin number to be set the first plugin |
| 2nd | sint8 | Plugin number to be set the second plugin |
| 3rd | sint8 | Plugin number to be set the third plugin |

When not specifying, set 0. If an 0 is placed mid-way, it will be moved to the front.  
Specifying zero plugin will result in an error.

### Properties

| Property | Requirement |
|:--|:--|
| Read | Mandatory |
| Write | Mandatory |
| Notify | Excluded |
