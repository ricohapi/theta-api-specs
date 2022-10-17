# camera.setOptions

### Overview

Property settings for shooting, the camera, etc.

Check the properties that can be set and specifications by the API v2.0 reference options category or [camera.getOptions](camera.get_options.md).

There is a detailed example of the request in [Getting Started.](../getting_started.md#3-acquireset-properties)

### Parameters

| Name | Type | Description |
|:--|:--|:--|
| sessionId | String | Session ID<br>Specify the value acquired by [camera.startSession](camera.start_session.md) |
| options | Object | Set of option names and setting values to be set in JSON format |

### Results

None

### Example

#### Parameters

```
{
    "sessionId": "12ABC3",
    "options": {
        "iso": 200
    }
}
```
