# 0x101C InitiateOpenCapture

### Operation Code

0x101C

### Overview

Starts continuous shooting.

In the still image shooting mode, interval shooting, interval composite shooting, multi bracket shooting, burst shooting, or continuous shooting starts.

In the movie shooting mode, movie shooting is started.

If [CaptureDelay](../property/capture_delay.md) is enabled, self-timer shooting starts.

Options are supported as follows:

| Operation Parameter | RICOH THETA specifications |
| --- | --- |
| StorageID | unused<br>Specify "0x00000000". |
| ObjectFormatCode | unused<br>Specify "0x00000000". |

### Support model

| X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|
| All | All | All | All | All |

### Support model

| Shooting mode | X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|:--|
| Interval shooting | All | All | All | All | All |
| Malti bracket shooting | All | All | All | v1.10 or later | v01.82 or later |
| Interval composite shooting | All | All | --- | v1.10 or later | v01.82 or later |
| Burst shooting | --- | v2.10.1 or later | --- | --- | --- |
| Continuous shooting | All | --- | --- | --- | --- |
| Self-timer shooting | All | All | All | All | All |
| Movie shooting | All | All | All | All | All |
| Movie self-timer shooting | All | All | v2.50.1 or later | --- | --- |
