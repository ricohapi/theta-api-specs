# Plugin Control

### Service

8AF982B1-F1FF-4D49-83F0-A56DB4C431A7

### Characteristic

A88732D5-6786-4312-9364-B9A4514DC123

### Overview

Starts or stops plugin. Also, acquires the plugin power status.  
RICOH THETA V firmware v2.21.1 and later.

### Value Fields

| Name | Type | Description |
| --- | --- | --- |
| Plugin Control | sint8 | Plugin power status (Kind of action)<br>(0: Running (Start plugin)、1: Stop) |
| Plugin | sint8 | Target plugin number. Set the target plugin number to [Plugin Orders](../camera_control_command/plugin_orders.md) before write. This parameter is ignored when Plugin Control parameter is 1 (stop).<br>RICOH THETA Z1 and later |

### Properties

| Property | Requirement |
|:--|:--|
| Read | Mandatory |
| Write | Mandatory |
| Notify | Mandatory |
