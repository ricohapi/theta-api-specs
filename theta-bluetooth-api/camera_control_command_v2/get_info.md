# Get Info

### Service

b6ac7a7e-8c01-4a52-b188-68d53df53ea2

### Characteristic

a0452e2d-c7d8-4314-8cd6-7b8bbab4d523

### Format

utf8s

### Overview

Acquires basic information of the camera and supported functions.

### Value Fields

| Name| Type | Description |
|:--|:--|:--|
|manufacturer|String|Manufacturer name
|model|String|Model
|serialNumber|String|Serial number
|_wlanMacAddress|String|MAC address of wireless LAN
|_bluetoothMacAddress|String|MAC address of Bluetooth
|firmwareVersion|String|Firmware version
|uptime|Integer|time after startup (sec)

```
Response (for RICOH THETA X)
{
    "_bluetoothMacAddress": "58:38:79:46:F7:61",
    "firmwareVersion": "2.20.1",
    "manufacturer": "Ricoh Company, Ltd.",
    "model": "RICOH THETA X",
    "serialNumber": "15001045",
    "_wlanMacAddress": "98:FE:94:45:D7:22",
    "uptime": 46
}
```

### Properties

| Property | Requirement |
|:--|:--|
| Read | Mandatory |
| Write | Excluded |
| Notify | Excluded |
