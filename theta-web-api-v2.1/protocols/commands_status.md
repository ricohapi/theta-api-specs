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

### Example (when state is inProgress)

#### Request

```
{
    "id": "90ABCD"
}
```

#### Response

```
{
    "name": "camera.startCapture",
    "state": "inProgress",
    "progress": {
      "completion": 0.02
    }
}
```

### Example (when state is done)

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
        "fileUrl": "http://192.168.1.1/files/abcde/100RICOH/R0010015.JPG"
    }
}
```
