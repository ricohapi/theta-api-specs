# Commands/Status

### API

POST /osc/commands/status

### Overview

Acquires the execution status of the command.

### Input

| Name | Type | Description |
|:--|:--|:--|
| id | String | Command ID acquired by [Commands/Execute](commands_execute.md) |

### Output

Same as the [Commands/Execute](commands_execute.md) output.

### Example

#### Request

```
{
    "id": "90ABCD"
}
```

#### Response

```
{
    "name": "camera.takePicture",
    "state": "done",
    "results": {
        "fileUri": "100RICOH/R0010015.JPG"
    }
}
```
