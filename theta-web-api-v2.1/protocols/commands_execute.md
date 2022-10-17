# Commands/Execute

### API

POST /osc/commands/execute

### Overview

Executes the command within the commands category.

### Input

| Name | Type | Description |
|:--|:--|:--|
| name | String | Command to execute |
| parameters | Object | Input parameters required to execute each command |

### Output

Either results, error, or progress is always returned in accordance with the execution status of the command.

The execution status of commands can be checked using [Commands/Status](commands_status.md).

| Name | Type | Description |
|:--|:--|:--|
| name | String | Executed command |
| state | String | Command execution status<br>Either "done", "inProgress" or "error" is returned |
| id | String | Command ID<br>Used to check the execution status with [Commands/Status](commands_status.md) |
| results | Object | Results when each command is successfully executed<br>This output occurs in state "done" |
| error | Object | Error information (See [Errors](errors.md) for details)<br>This output occurs in state "error" |
| progress | Object | Progress<br>This output occurs in state "inProgress"<br>Details in the following item |

### progress object

| Name | Type | Description |
|:--|:--|:--|
| completion | Number | Progress rate of command executed |

### Example (when state is inProgress)

#### Request

```
{
    "name": "camera.startCapture",
    "parameters": {
      "_mode": "composite"
    }
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
    "name": "camera.getOptions",
    "parameters": {
        "optionNames": [
            "exposureProgram",
            "exposureProgramSupport"
        ]
    }
}
```

#### Response

```
{
    "name": "camera.getOptions",
    "state": "done",
    "results": {
      "options": {
        "exposureProgram": 2,
        "exposureProgramSupport": [1, 2, 4, 9]
      }
    }
}
```
