# Overview

For RICOH THETA V and Z1, camera control such as shooting via Bluetooth Low Energy communication is available. The communication protocol is implemented according to the Bluetooth 4.2 Core Specifications including RICOH THETA Extensions.

Obtain the base specifications from the following:

- [Bluetooth 4.2 Core Specifications](https://www.bluetooth.org/DocMan/handlers/DownloadDoc.ashx?doc_id=286439&_ga=2.97979420.260081372.1496207139-937189733.1496207139)

### Bluetooth authentication

1. Turn BLE ON with [\_bluetoothPower](../theta-web-api-v2.1/options/_bluetooth_power.md)
1. Send UUID with [camera.\_setBluetoothDevice](../theta-web-api-v2.1/commands/camera._set_bluetooth_device.md)
1. Search for the Bluetooth device with deviceName obtained in step 2
1. Set the same UUID as in step 2 with [Auth Bluetooth Device](bluetooth_control_command/auth_bluetooth_device.md)
