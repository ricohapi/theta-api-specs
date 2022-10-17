# Burst Option

### Service

38EF1533-B0CC-4722-B6B6-8B23C27ECE5C

### Characteristic

A7E6BF19-F3C2-4A89-BD57-3AB5C2D06052

### Format

sint8

### Overview

Burst shooting setting.

### Value Fields

| Name | Type | Description |
|:--|:--|:--|
| burstCaptureNum | sint8 | Number of shots for burst shooting |
| burstBracketStep | sint8 | Bracket value range between each shot for burst shooting |
| burstCompensation | sint8 | Exposure compensation for the base image and entire shooting for burst shooting |
| burstMaxExposureTime | sint8 | Maximum exposure time for burst shooting |
| burstEnableISOControl | sint8 | Adjustment with ISO sensitivity for burst shooting |
| burstOrder | sint8 | Shooting order for burst shooting |

#### burstCaptureNum

| Value | Description |
|:--|:--|
| 1 | 1 |
| 3 | 3 |
| 5 | 5 |
| 7 | 7 |
| 9 | 9 |

#### burstBracketStep

| Value | Description |
|:--|:--|
| 0 | 0.0Ev |
| 1 | 0.3Ev |
| 2 | 0.7Ev |
| 3 | 1.0Ev |
| 4 | 1.3Ev |
| 5 | 1.7Ev |
| 6 | 2.0Ev |
| 7 | 2.3Ev |
| 8 | 2.7Ev |
| 9 | 3.0Ev |

#### burstCompensation

| Value | Description |
|:--|:--|
| -15 | -5.0Ev |
| -14 | -4.7Ev |
| -13 | -4.3Ev |
| -12 | -4.0Ev |
| -11 | -3.7Ev |
| -10 | -3.3Ev |
| -9 | -3.0Ev |
| -8 | -2.7Ev |
| -7 | -2.3Ev |
| -6 | -2.0Ev |
| -5 | -1.7Ev |
| -4 | -1.3Ev |
| -3 | -1.0Ev |
| -2 | -0.7Ev |
| -1 | -0.3Ev |
| 0 | 0.0Ev |
| 1 | 0.3Ev |
| 2 | 0.7Ev |
| 3 | 1.0Ev |
| 4 | 1.3Ev |
| 5 | 1.7Ev |
| 6 | 2.0Ev |
| 7 | 2.3Ev |
| 8 | 2.7Ev |
| 9 | 3.0Ev |
| 10 | 3.3Ev |
| 11 | 3.7Ev |
| 12 | 4.0Ev |
| 13 | 4.3Ev |
| 14 | 4.7Ev |
| 15 | 5.0Ev |

#### burstMaxExposureTime

| Value | Description |
|:--|:--|
| 41 | 1/2sec |
| 42 | 1/1.6sec |
| 43 | 1/1.3sec |
| 44 | 1sec |
| 45 | 1.3sec |
| 46 | 1.6sec |
| 47 | 2sec |
| 48 | 2.5sec |
| 49 | 3.2sec |
| 50 | 4sec |
| 51 | 5sec |
| 52 | 6sec |
| 53 | 8sec |
| 54 | 10sec |
| 55 | 13sec |
| 56 | 15sec |
| 57 | 20sec |
| 58 | 25sec |
| 59 | 30sec |
| 60 | 40sec |
| 61 | 50sec |
| 62 | 60sec |

#### burstEnableISOControl

| Value | Description |
|:--|:--|
| 0 | Do not adjust with ISO sensitivity |
| 1 | Adjust with ISO sensitivity |

#### burstOrder

| Value | Description |
|:--|:--|
| 0 | '0'→'-'→'+' |
| 1 | '-'→'0'→'+' |

### Properties

| Property | Requirement |
|:--|:--|
| Read | Mandatory |
| Write | Mandatory |
| Notify | Excluded |
