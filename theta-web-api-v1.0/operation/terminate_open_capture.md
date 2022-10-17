# 0x1018 TerminateOpenCapture

### Operation Code

0x1018

### Overview

Exit continuous shooting for the specified TransactionID.

To exit all continuous shooting, specify 0xFFFFFFFF as the TransactionID.

The video recording stop sound is not emitted in the following cases.

- When the [video recording time](../property/recording_time.md) reaches the [remaining recording time](../property/remaining_recording_time.md) limit
- When a [warning or error](../property/error_info.md) occurs during recording

### Prohibited Operations

If the TerminateOpenCapture operation is requested under any of the following conditions, the reply is the CaptureAlreadyTerminated response because the operation has already ended.

- [StillCaptureMode](../property/still_capture_mode.md) is in single shot mode
- [StillCaptureMode](../property/still_capture_mode.md) has not started interval shooting mode or interval shooting
- Shooting mode has not started video shooting mode or video recording
