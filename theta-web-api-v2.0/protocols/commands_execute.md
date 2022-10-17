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
| progress | Object | Progress<br>This output occurs in state "inProgress" |

### Example

#### Request

```
{
    "name": "camera.getOptions",
    "parameters": {
        "sessionId": "12ABC3",
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
