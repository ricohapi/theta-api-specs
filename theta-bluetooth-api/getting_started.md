# Getting Started

For RICOH THETA V and Z1, camera control such as shooting via Bluetooth Low Energy communication is available.

This section explains the following flow for shooting a still image.

1. [Bluetooth authentication](#1-bluetooth-authentication)
1. [Acquire and set shooting properties](#2-acquire-and-set-shooting-properties)
1. [Shoot a still image](#3-shoot-a-still-image)
1. [Check for file saving](#4-check-for-file-saving)
1. [Wake camera up from sleep](#5-wake-camera-up-from-sleep)

Below, the Bluetooth device is called Central device, RICOH THETA is called Peripheral device.

### 1. Bluetooth authentication

RICOH THETA authenticates a central device via Web API and Bluetooth API. The camera does not use pairing.

Register the central device UUID to camera from Web API command [camera.\_setBluetoothDevice](../theta-web-api-v2.1/commands/camera._set_bluetooth_device.md), and turn the Bluetooth module ON with option [\_bluetoothPower](../theta-web-api-v2.1/options/_bluetooth_power.md).

#### Request (Register a central device)

```
POST /osc/commands/execute
{
    "name": "camera._setBluetoothDevice",
    "parameters": {
        "uuid": "01234567-89ab-cdef-0123-456789abcdef"
    }
}
```

#### Response

```
{
    "name": "camera._setBluetoothDevice",
    "state": "done",
    "results": {
        "deviceName": "00101234"
    }
}
```

#### Request (Bluetooth power ON)

```
POST /osc/commands/execute
{
    "name": "camera.setOptions",
    "parameters": {
        "options": {
            "_bluetoothPower": "ON"
        }
    }
}
```

#### Response

```
{
    "name": "camera.setOptions",
    "state": "done"
}
```

Search for the camera with deviceName obtained in registration, and set the central device UUID via Bluetooth API to authenticate.  
 Use [Auth Bluetooth Device](bluetooth_control_command/auth_bluetooth_device.md) via Bluetooth API.

#### Write (Authenticate the central device)

```
Service: "0F291746-0C80-4726-87A7-3C501FD3B4B6" (Bluetooth Control Command)
Characteristic: "EBAFB2F0-0E0F-40A2-A84F-E2F098DC13C3" (Auth Bluetooth Device)
Property: Write
Value: "01234567-89ab-cdef-0123-456789abcdef"
```

### 2. Acquire and set shooting properties

Acquire the shooting properties.

The following shows an example of acquiring the ISO sensitivity ([ISO](shooting_control_command/iso.md).)

#### Read

```
Service: "1D0F3602-8DFB-4340-9045-513040DAD991" (Shooting Control Command)
Characteristic: "ABB94D51-189F-455B-951D-ABE9B0333080" (ISO)
Property: Read
```

#### Response

```
    0x4001
```

Set the shooting properties.

The following shows an example of setting ISO sensitivity to 400.

#### Write

```
Service: "1D0F3602-8DFB-4340-9045-513040DAD991" (Shooting Control Command)
Characteristic: "ABB94D51-189F-455B-951D-ABE9B0333080" (ISO)
Property: Write
Value: 0x9001
```

### 3. Shoot a still image

Operate the shutter. The command used depends on whether still images are shot by single shooting or continuous shooting.

Set [File Format](shooting_control_command/file_format.md) and [Capture Mode](shooting_control_command/capture_mode.md) at first, and shoot a single still image by command [Take Picture](shooting_control_command/take_picture.md) or shoot images or video continuously by command [Continuous Shooting](shooting_control_command/continuous_shooting.md). The example for single still image shooting is as follows.

#### Write (Set still image format)

```
Service: "1D0F3602-8DFB-4340-9045-513040DAD991" (Shooting Control Command)
Characteristic: "E8F0EDD1-6C0F-494A-95C3-3244AE0B9A01" (File Format)
Property: Write
Value: 0x00
```

#### Write (Set still capture mode)

```
Service: "1D0F3602-8DFB-4340-9045-513040DAD991" (Shooting Control Command)
Characteristic: "78009238-AC3D-4370-9B6F-C9CE2F4E3CA8" (Capture Mode)
Property: Write
Value: 0x00
```

#### Write (Shoot a still image)

```
Service: "1D0F3602-8DFB-4340-9045-513040DAD991" (Shooting Control Command)
Characteristic: "FEC1805C-8905-4477-B862-BA5E447528A5" (Take Picture)
Property: Write
Value: 0x01
```

### 4. Check for file saving

The shooting status notification tells us completion of file save: [Take Picture](shooting_control_command/take_picture.md) for single still image or [Continuous Shooting](shooting_control_command/continuous_shooting.md) for continuous shooting. The notification does not depend on the type of API. For example, the shooting status notification will be changed by shutter button of the camera.

#### Notify (Status of still image shooting)

```
Service: "1D0F3602-8DFB-4340-9045-513040DAD991" (Shooting Control Command)
Characteristic: "FEC1805C-8905-4477-B862-BA5E447528A5" (Take Picture)
Property: Notify
Value: 0x00
```

### 5. Wake camera up from sleep

Some services become disabled when the camera goes to sleep. In that case, wake the camera up by [Camera Power](camera_status_command/camera_power.md) and start from 1. Bluetooth authentication again.

#### Write

```
Service: "8AF982B1-F1FF-4D49-83F0-A56DB4C431A7" (Camera Status Command)
Characteristic: "B58CE84C-0666-4DE9-BEC8-2D27B27B3211" (Camera Power)
Property: Write
Value: 0x01
```
