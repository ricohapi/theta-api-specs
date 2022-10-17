# camera.updateSession

### Overview

Updates the session. Extends the validity period of the session.

### Parameters

| Name | Type | Description |
|:--|:--|:--|
| sessionId | String | Session ID<br>Specify the value acquired by [camera.startSession](camera.start_session.md) |

### Results

| Name | Type | Description |
|:--|:--|:--|
| sessionId | String | Session ID |
| timeout | Integer | Time during which the session is enabled (sec.)<br>Fixed value: 180 |
