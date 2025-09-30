# ISO

### Service

1D0F3602-8DFB-4340-9045-513040DAD991

### Characteristic

ABB94D51-189F-455B-951D-ABE9B0333080

### Format

sint16

### Overview

Acquires or sets the ISO sensitivity.

It can be set for video shooting mode at RICOH THETA V firmware v3.00.1 and later. Shooting settings are retained separately for both the Still image shooting mode and Video shooting mode.

### Value Fields

#### When the exposure program ([Exposure Program](exposure_program.md)) is set to Manual or ISO Priority

##### For RICOH THETA Z1 and later

80, 100, 125, 160, 200, 250, 320, 400, 500, 640, 800, 1000, 1250, 1600, 2000, 2500, 3200, 4000, 5000, 6400

##### For RICOH THETA V

64, 80, 100, 125, 160, 200, 250, 320, 400, 500, 640, 800, 1000, 1250, 1600, 2000, 2500, 3200, 4000\*, 5000\*, 6000\*

\* Available in Video shooting mode.

#### Otherwise

0（AUTO）

### Properties

| Property | Requirement |
|:--|:--|
| Read | Mandatory |
| Write | Mandatory |
| Notify | Excluded |
