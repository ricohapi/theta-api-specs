# 0x99A9 GetPluginInfo

### Operation Code

0x99A9

### Overview

Return the detailed plugin information.  
(Vendor Extension Operations)

Operation Parameters as follows.

| No. | Operation Parameter | RICOH THETA Specification |
|:--|:--|:--|
| 1 | PluginHandle | Plugin handle of the target plugin |
| 2 | Reserved | unused<br>Specify 0x00000000 |
| 3 | Reserved | unused<br>Specify 0x00000000 |
| 4 | Reserved | unused<br>Specify 0x00000000 |
| 5 | Reserved | unused<br>Specify 0x00000000 |

### Support model

| X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|
| All | All | v2.21.1 or later | --- | --- |

### Support value

The plugin information format is predetermined by the following.

\<PluginName\>\<PackageName\>\<Version\>\<Type\>\<Running\>\<Foreground\>\<Boot\>\<Reserved1\>\<Reserved2\>\<WebServer\>\<ExitStatus\>\<Message\>

| Name | Size | Data Type | Description |
|:--|:--|:--|:--|
| PluginName | any | String | Plugin name |
| PackageName | any | String | Package name |
| Version | any | String | Plugin version |
| Type | 1 | UINT8 | The kind of application<br>(0: Pre-installed plugin, 1: User-added plugin) |
| Running | 1 | UINT8 | Plugin power status<br>(0: running, 1: stop) |
| Foreground | 1 | UINT8 | Process status<br>(0: foreground, 1: background) |
| Boot | 1 | UINT8 | Boot selection<br>(0: Target plugin to be started; 1: Do not start this plugin) |
| Reserved1 | 1 | UINT8 | Reserved |
| Reserved2 | any | String | Reserved |
| WebServer | 1 | UINT8 | Existence of web server<br>(0: Has WebUI, 1: Does not have WebUI) |
| ExitStatus | 1 | UINT8 | Exit status<br>(0: seccess, 1: error) |
| Message | any | String | Message |
