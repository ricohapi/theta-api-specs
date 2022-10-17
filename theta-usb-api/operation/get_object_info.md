# 0x1008 GetObjectInfo

### Operation Code

0x1008

### Overview

Returns the object information for the specified object handle.

For EXIF/JPG data, the interval shooting group ID (17 bytes) or interval composite group shooting group ID (17 bytes, RICOH THETA Z1, RICOH THETA S firmware v01.82 or later and RICOH THETA SC firmware v1.10 or later), or multi bracket shooting group ID (17 bytes, RICOH THETA Z1, RICOH THETA V, RICOH THETA S firmware v01.82 or later and RICOH THETA SC firmware v1.10 or later) is returned in "keywords".

Duplicate group IDs may be recorded in the following cases:

- Time is not set correctly.
- Camera was used in different time zones.

### Support model

| X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|
| All | All | All | All | All |
