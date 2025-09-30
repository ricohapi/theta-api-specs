# \_bluetoothClassicEnable

### Overview

Status of enable/disable Bluetooth Classic.

Can be acquired by [camera.getOptions](../commands/camera.get_options.md) and set by [camera.setOptions](../commands/camera.set_options.md).

Under the following conditions, in order to apply set value, [_bluetoothPower](_bluetooth_power.md) is power cycled.
- [_bluetoothPower](_bluetooth_power.md) is ON
- Set a value differed in current value

### Support model

| X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|
| --- | v1.50.1 and later | v3.40.1 and later | --- | --- |

This option is available for THETA Plugin only.

\<Note\>  
This option cannot be accessed from outside of THETA. This option need to be accessed from THETA Plugin.    
Otherwise, this option returns error with the code: invalidParameterValue. (RICOH THETA Z1 firmware v1.50.1 and RICOH THETA V firmware v3.40.1; This option returns false.)    

### Support value

| Value | Description |
|:--|:--|
| true | Enable Bluetooth Classic status |
| false | Disable Bluetooth Classic status |
