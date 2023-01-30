# THETA Firmware History

## THETA Z1 firmware v2.20.3 (2023.1.31)

### WebAPI
* [State](../theta-web-api-v2.1/protocols/state.md) : Update new error code HIGH_TEMPERATURE_WARNING
* [_whiteBalanceAutoStrength](../theta-web-api-v2.1/options/_white_balance_auto_strength.md) : New Added

### Bluetooth API
* [Camera Error](../theta-bluetooth-api/shooting_status_command/camera_error.md) : Update new error code HIGH_TEMPERATURE_WARNING
* [White Balance Auto Strength](../theta-bluetooth-api/shooting_control_command_v2/white_balance_auto_strength.md) : New Added
* [My Setting](../theta-bluetooth-api/shooting_control_command/my_setting.md) : Update new option White Balance Auto Strength
 
### USB-API
* [0xD006 ErrorInfo](../theta-usb-api/property/error_info.md) : Update new error code HIGH_TEMPERATURE_WARNING
* [0xD83A White Balance Auto Strength](../theta-usb-api/property/white_balance_auto_strength.md) : New Added

### Plugin
* [Camera API](../ricoh-theta-plugin/camera-api.md#white-balance-auto-strength) : Update new Key RIC_WB_STRENGTH

## THETA X firmware v1.40.0 (2022.12.20)

### WebAPI
* [_bitrate](../theta-web-api-v2.1/options/_bitrate.md) : Update bitrate setting table
* [_networkType](../theta-web-api-v2.1/options/_network_type.md) : Update
* [State](../theta-web-api-v2.1/protocols/state.md) : Update new error code HIGH_TEMPERATURE_WARNING
* [_waterHousing](../theta-web-api-v2.1/options/_water_housing.md) : New added
* [_waterHousingStitching](../theta-web-api-v2.1/options/_water_housing_stitching.md) : New added
* [whiteBalance](../theta-web-api-v2.1/options/white_balance.md) : Update description of _underwater
 
### USB-API
* [0xD829 Bitrate](../theta-usb-api/property/bitrate.md) : Update bitrate setting table
* [0xD006 ErrorInfo](../theta-usb-api/property/error_info.md) : Update new error code HIGH_TEMPERATURE_WARNING
* [0xD83B Water Housing](../theta-usb-api/property/water_housing.md) : New Added
* [0xD83C Water Housing Stitching](../theta-usb-api/property/water_housing_stitching.md) : New Added
* [0x5005 White Balance](../theta-usb-api/property/white_balance.md) : Update description of Underwater

### Plugin
* [Broadcast Intent](../ricoh-theta-plugin/broadcast-intent.md#disable-power-button-feature) : Update new intent com.theta360.plugin.ACTION_ENABLE(DISABLE)_POWER_BUTTON
* [Camera API](../ricoh-theta-plugin/camera-api.md#stitching) : Update new Key RIC_WATER_HOUSING
