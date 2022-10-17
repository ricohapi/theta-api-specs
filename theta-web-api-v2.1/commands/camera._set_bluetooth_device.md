# camera.\_setBluetoothDevice

### Overview

Registers identification information (UUID) of a BLE device (Smartphone application) connected to the camera to the camera. UUID can be set while the wireless LAN function of the camera is placed in the direct mode.

### Support model

| X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|
| --- | All | All | --- | --- |

### Parameters

| Name | Type | Description |
|:--|:--|:--|
| uuid | String | Format: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx<br>Alphabetic letters are not case-sensitive. |

### Results

| Name | Type | Description |
|:--|:--|:--|
| deviceName | String | Device name is generated from the serial number (S/N) of the camera.<br>[Example] "00101234" or "THETAXS00101234" when the serial number (S/N) is "XS00101234" |
