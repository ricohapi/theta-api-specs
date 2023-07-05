# Get State2

### Service

b6ac7a7e-8c01-4a52-b188-68d53df53ea2

### Characteristic

8881ce4e-96fc-4c6c-8103-5dda0ad138fb

### Format

utf8s

### Overview

Acquires the camera states.

### Value Fields

| Name| Type | Description |
|:--|:--|:--|
| \_externalGpsInfo | gpsInfo | gpsInfo set by API. |
| \_internalGpsInfo | gpsInfo | gpsInfo from the built-in GPS module. |

```
Response (for RICOH THETA X)
{
    "_externalGpsInfo": {
        "gpsInfo": {
            "_altitude": 0,
            "_dateTimeZone": "",
            "_datum": "",
            "lat": 65535,
            "lng": 65535
        }
    },
    "_internalGpsInfo": {
        "gpsInfo": {
            "_altitude": 0,
            "_dateTimeZone": "",
            "_datum": "",
            "lat": 65535,
            "lng": 65535
        }
    }
}
```

### Properties

| Property | Requirement |
|:--|:--|
| Read | Mandatory |
| Write | Excluded |
| Notify | Excluded |
