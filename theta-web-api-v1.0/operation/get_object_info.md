# 0x1008 GetObjectInfo

### Operation Code

0x1008

### Overview

Return object information for the specified ObjectHandle.

Interval shooting group ID (17 bytes) are returned as keywords in the case of EXIF/JPG.

However, duplicate interval shooting group IDs may be recorded under the following conditions.

- When the clock is not set correctly
- When the RICOH THETA is used in different time zones
