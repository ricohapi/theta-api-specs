# Command Error Description

### Service

8AF982B1-F1FF-4D49-83F0-A56DB4C431A7

### Characteristic

4B03D05E-02D2-412B-A20B-578AE82B9C01

### Format

sint8

### Overview

Acquires the camera's error description in detail.

### Value Fields

| Value | Description |
|:--|:--|
| 0 | Disabled Command<br>Command cannot be executed due to the camera status |
| 1 | Missing Parameter<br>Insufficient required parameters to issue the command |
| 2 | Invalid Parameter Value<br>Parameter value when command was issued is invalid |
| 3 | Power Off Sequence Running<br>Process request when power supply is off |
| 4 | Invalid File Format<br>Invalid file format specified |
| 5 | Service Unavailable<br>Processing requests cannot be received temporarily |
| 6 | Device Busy |
| 7 | Unexpected<br>Other errors |

### Properties

| Property | Requirement |
|:--|:--|
| Read | Excluded |
| Write | Excluded |
| Notify | Mandatory |
