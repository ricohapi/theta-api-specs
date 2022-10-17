# CheckForUpdates

### API

POST /osc/checkForUpdates

### Overview

Acquires the current status ID, and checks for changes to the [State](state.md) status.

### Input

| Name | Type | Description |
|:--|:--|:--|
| stateFingerprint | String | Status ID |

### Output

| Name | Type | Description |
|:--|:--|:--|
| stateFingerprint | String | Current status ID |

### Example

#### Request

```
{
    "stateFingerprint": "12EGA33"
}
```

#### Response

```
{
    "stateFingerprint": "12EGA86"
}
```
