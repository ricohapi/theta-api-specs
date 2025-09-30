# Shooting Method

### Service

38EF1533-B0CC-4722-B6B6-8B23C27ECE5C

### Characteristic

8FBDFAD4-CE9B-4A10-9F2D-DEE7929ED14E

### Format

sint8

### Overview

Acquires and sets the shooting method for My Settings mode.  
Can be acquired and set only when in the Still image shooting mode and \_function is the My Settings shooting function.  
Changing \_function initializes the setting details to Normal shooting.  
RICOH THETA Z1 and later

### Value Fields

| Value | Description |
|:--|:--|
| 0 | Normal shooting |
| 1 | Interval shooting |
| 2 | Multi bracket shooting |
| 3 | Interval composite shooting |
| 4 | Move interval shooting \*1 |
| 5 | Fixed interval shooting \*1 |
| 6 | Burst shooting \*2 |

\*1 RICOH THETA Z1 v1.50.1 and later  
\*2 RICOH THETA Z1 v2.10.1 and later  

### Properties

| Property | Requirement |
|:--|:--|
| Read | Mandatory |
| Write | Mandatory |
| Notify | Excluded |
