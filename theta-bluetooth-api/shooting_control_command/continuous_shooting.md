# Continuous Shooting

### Service

1D0F3602-8DFB-4340-9045-513040DAD991

### Characteristic

E33B80DC-4661-458F-B873-AC5270F8AB5C

### Format

sint8

### Overview

Starts and stops interval shooting, bracketing, interval composite, time shift shooting, burst shooting, or movie shooting. Also, acquires the shooting status.

### Value Fields

| Value | Description |
|:--|:--|
| 0 | Standby for shooting (Shooting stopped \* Continuous shooting should have been started. Shooting cannot be interrupted during burst shooting.) |
| 1 | Performing movie shooting in progress (Movie shooting started \* Camera should in the movie shooting mode.) |
| 2 | Performing interval shooting (Interval shooting started \* Camera should in the still image shooting mode.) |
| 3 | Performing bracketing (Bracketing started \* Camera should in the still image shooting mode.) |
| 4 | Conversion of a saved movie ([camera.\_convertVideoFormats](../../theta-web-api-v2.1/commands/camera._convert_video_formats.md)) in progress.<br>Writing is Excluded. |
| 5 | Performing interval composite shooting (Interval composite shooting started \* Camera should in the still image shooting mode.)<br>RICOH THETA Z1 and later |
| 6 | Performing time shift shooting.<br>RICOH THETA Z1 and RICOH THETA V firmware v3.00.1 and later<br>Writing is Excluded. |
| 7 | Performing interval shooting (optimized \*1, Tripod stabilization Off) (Interval shooting started \* Camera should in the still image shooting mode.)<br>RICOH THETA Z1 v1.50.1 and later and RICOH THETA V firmware v3.40.1 and later |
| 8 | Performing interval shooting (optimized \*1, Tripod stabilization On) (Interval shooting started \* Camera should in the still image shooting mode.)<br>RICOH THETA Z1 v1.50.1 and later and RICOH THETA V firmware v3.40.1 and later |
| 9 | Performing burst shooting(Burst shooting started \* Camera should in the still image shooting mode.)<br>RICOH THETA Z1 v2.10.1 and later |

\*1 Top/bottom correction and stitching conditions are optimized.

### Properties

| Property | Requirement |
|:--|:--|
| Read | Mandatory |
| Write | Mandatory |
| Notify | Mandatory |
