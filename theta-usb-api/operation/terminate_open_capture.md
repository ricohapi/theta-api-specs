# 0x1018 TerminateOpenCapture

### Operation Code

0x1018

### Overview

Exit continuous shooting for the specified TransactionID.

Specify 0xFFFFFFFF as the TransactionID.

Shooting cannot be interrupted during burst shooting.  

The video recording stop sound is not emitted in the following cases.

- When the [video recording time](../property/recording_time.md) reaches the [remaining recording time](../property/remaining_recording_time.md) limit
- When a [warning or error](../property/error_info.md) occurs during recording

### Support model

| X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|
| All | All | All | All | All |

### Prohibited Operations

If the TerminateOpenCapture operation is requested without starting a continuous shooting, the reply is the CaptureAlreadyTerminated response because the operation has already ended.
