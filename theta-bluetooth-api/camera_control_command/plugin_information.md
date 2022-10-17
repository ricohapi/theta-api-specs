# Plugin Information

### Service

32886D39-BA23-425C-BCAE-9C1DB0066922

### Characteristic

E7FFAD40-8049-4028-AFC0-FDD8DE8F67DE

### Overview

Acquires the detailed plugin information applicable in [Selected Plugin.](selected_plugin.md)  
RICOH THETA V firmware v2.21.1 or later.

### Value Fields

| Name | Type | Description |
|:--|:--|:--|
| Package Name Length | sint8 | Length of package name |
| Plugin Name Length | sint8 | Length of plugin name |
| Version Length | sint8 | Length of version |
| Package Name | utf8s | Package name |
| Plugin Name | utf8s | Plugin name |
| Version | utf8s | Plugin version |
| Type | sint8 | The kind of application<br>(0: Pre-installed plugin, 1: User-added plugin) |

### Properties

| Property | Requirement |
|:--|:--|
| Read | Mandatory |
| Write | Excluded |
| Notify | Excluded |
