# Top Bottom Correction

### Service

38EF1533-B0CC-4722-B6B6-8B23C27ECE5C

### Characteristic

FD2F10FC-22A2-42C9-B5EF-325228D02D69

### Format

sint16

### Overview

Acquires and sets the top/bottom correction setting for still image.  
RICOH THETA V firmware v3.00.1 and later.

### Value Fields

| Value | Description |
|:--|:--|
| 0 | Top/bottom correction is performed. |
| 1 | Top/bottom correction is performed. However, for Interval shooting, the parameters used for top/bottom correction for the first image are saved and used for the 2nd and subsequent images. |
| 2 | Performs top/bottom correction and then saves the parameters. |
| 3 | Performs top/bottom correction using the saved parameters. |
| 4 | Does not perform top/bottom correction. |

### Properties

| Property | Requirement |
|:--|:--|
| Read | Mandatory |
| Write | Mandatory |
| Notify | Excluded |
