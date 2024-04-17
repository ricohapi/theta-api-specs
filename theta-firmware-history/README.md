# THETA Firmware History

## THETA X firmware v2.50.2 (2024.04.18)

### WebAPI
* [fileFormat](../theta-web-api-v2.1/options/file_format.md) : Update new video mode
* [_gain](../theta-web-api-v2.1/options/_gain.md) : Update new value `mute`
* [_hdrBracket](../theta-web-api-v2.1/options/_hdr_bracket.md) : New Added

### USB-API
* [0x5003](../theta-usb-api/property/image_size.md) : Update new video mode
* [0xD81F Gain](../theta-usb-api/property/gain.md) : Update new value `mute`
* [0xD840 hdrBracket](../theta-usb-api/property/hdr_bracket.md) : New Added

### Plugin
* [HDR Bracket Setting](../ricoh-theta-plugin/camera-api.md#hdr-bracket-setting) : Update new Key `RIC_HDR_BRACKET`

## THETA X firmware v2.40.0 (2024.01.16)

### WebAPI
* [State](../theta-web-api-v2.1/protocols/state.md#_cameraerror) : Update new error code `COMPASS CALIBRATION`, and Update `_cameraError` table
* [_autoBracket](../theta-web-api-v2.1/options/_auto_bracket.md) : Update spec
* [_filter](../theta-web-api-v2.1/options/_filter.md) : Update new value `Hh HDR` for Handheld HDR
* [_ethernetConfig](../theta-web-api-v2.1/options/_ethernet_config.md) : New Added

### USB-API
* [0xD812 BracketParameters](../theta-usb-api/property/bracket_parameters.md) : Update spec
* [0xD80B Filter](../theta-usb-api/property/filter.md) : Update new value `0x04` for Handheld HDR

### Plugin
* [Camera API](../ricoh-theta-plugin/camera-api.md#shooting-mode) : Update new parameter `RicStillCaptureYuvHhHDR`

### Others
* [THETA Metadata Spec](../theta-metadata/README.md#rdt-atom) : Update spec of `RDTL` header

## THETA X firmware v2.30.0 (2023.10.17)

### Plugin
* [Broadcast Intent](../ricoh-theta-plugin/broadcast-intent.md#power-off) : Update new intent com.theta360.plugin.ACTION_POWER_OFF

## THETA X firmware v2.21.0 (2023.08.22)

No API Update

## THETA Z1 firmware v3.10.2 (2023.08.01)

### WebAPI
* [State](../theta-web-api-v2.1/protocols/state.md) : Update new options "\_externalGpsInfo", "\_internalGpsInfo", "\_boardTemp", and "\_batteryTemp"

### Bluetooth-API
* [Get Info](../theta-bluetooth-api/camera_control_command_v2/get_info.md) : New Added
* [Get State](../theta-bluetooth-api/camera_control_command_v2/get_state.md) : New Added
* [Get State2](../theta-bluetooth-api/camera_control_command_v2/get_state2.md) : New Added
* [Notify State](../theta-bluetooth-api/camera_control_command_v2/notify_state.md) : New Added

### USB-API
* [0xD83E ExposureStatus](../theta-usb-api/property/exposure_status.md) : New Added
  
## THETA X firmware v2.20.1 (2023.07.25)

### WebAPI
* [State](../theta-web-api-v2.1/protocols/state.md) : Update new options "\_externalGpsInfo", "\_internalGpsInfo", "\_boardTemp", and "\_batteryTemp"

### Bluetooth-API
* [Get Info](../theta-bluetooth-api/camera_control_command_v2/get_info.md) : New Added
* [Get State](../theta-bluetooth-api/camera_control_command_v2/get_state.md) : New Added
* [Get State2](../theta-bluetooth-api/camera_control_command_v2/get_state2.md) : New Added
* [Notify State](../theta-bluetooth-api/camera_control_command_v2/notify_state.md) : New Added

### Plugin
* [Broadcast Intent](../ricoh-theta-plugin/broadcast-intent.md#control-battery-charging) : Update new intent com.theta360.plugin.ACTION_BATTERY_CHARGING_SUSPEND(RESUME)

## THETA Z1 firmware v3.01.1 (2023.06.27)

### WebAPI
* [camera.listFiles](../theta-web-api-v2.1/commands/camera.list_files.md) : Update description of entries object "_projectionType". Update entries object "_frameRate"
* [fileFormat](../theta-web-api-v2.1/options/file_format.md) : Update new option video format
* [_maxRecordableTime](../theta-web-api-v2.1/options/_max_recordable_time.md) : Update new 50 minutes setting only for 3.6K 1/2fps and 2.7K 1/2fps.

### USB-API
* [0x5003 ImageSize](../theta-usb-api/property/image_size.md) : Update new option movie shooting mode
* [0xD823 MaxRecordableTime](../theta-usb-api/property/max_recordable_time.md) : Update new 50 minutes setting only for 3.6K 1/2fps and 2.7K 1/2fps.

### Bluetooth-API
* [File Format](../theta-bluetooth-api/shooting_control_command/file_format.md) : Update new option video format
* [Max Recordable Time](../theta-bluetooth-api/shooting_control_command/max_recordable_time.md) : Update new 50 minutes setting only for 3.6K 1/2fps and 2.7K 1/2fps.

## THETA X firmware v2.10.1 (2023.06.19)

No API Update

## THETA X firmware v2.00.0 (2023.04.12)

### WebAPI

* [_bitrate](../theta-web-api-v2.1/options/_bitrate.md) : Update bitrate setting table
* [listFiles](../theta-web-api-v2.1/commands/camera.list_files.md) : Update new parameter "_storage" and new entries object "_storageID"
* [_maxRecordableTime](../theta-web-api-v2.1/options/_max_recordable_time.md) : Update new 120 minutes setting only for 5.7K 2/5/10fps and 8K 2/5/10fps.
* [previewFormat](../theta-web-api-v2.1/options/preview_format.md) : Update spec
* [_proxy](../theta-web-api-v2.1/options/_proxy.md) : New Added
* [_setAccessPoint](../theta-web-api-v2.1/commands/camera._set_access_point.md) : Update new option _proxy
* [_listAccessPoints](../theta-web-api-v2.1/commands/camera._list_access_points.md) : Update new option _proxy

### USB-API

* [0xD829 Bitrate](../theta-usb-api/property/bitrate.md) : Update bitrate setting table
* [0xD823 MaxRecordableTime](../theta-usb-api/property/max_recordable_time.md) : Update new 120 minutes setting. Only for 5.7K 2/5/10fps and 8K 2/5/10fps.

### Plugin
* [Broadcast Intent](../ricoh-theta-plugin/broadcast-intent.md#disable-power-button-feature) : Update new intent com.theta360.plugin.ACTION_BLUETOOTH_ON(OFF) and com.theta360.plugin.ACTION_GPS_ON(OFF)

## THETA Z1 firmware v2.30.1 (2023.02.28)

No API Update

## THETA X firmware v1.41.0 (2023.01.24)

No API Update

## THETA Z1 firmware v2.20.3 (2023.1.31)

### WebAPI
* [State](../theta-web-api-v2.1/protocols/state.md) : Update new error code HIGH_TEMPERATURE_WARNING
* [_whiteBalanceAutoStrength](../theta-web-api-v2.1/options/_white_balance_auto_strength.md) : New Added
* [_proxy](../theta-web-api-v2.1/options/_proxy.md) : New Added
* [_setAccessPoint](../theta-web-api-v2.1/commands/camera._set_access_point.md) : Update new option _proxy
* [_listAccessPoints](../theta-web-api-v2.1/commands/camera._list_access_points.md) : Update new option _proxy

### Bluetooth API
* [Camera Error](../theta-bluetooth-api/shooting_status_command/camera_error.md) : Update new error code HIGH_TEMPERATURE_WARNING
* [White Balance Auto Strength](../theta-bluetooth-api/shooting_control_command_v2/white_balance_auto_strength.md) : New Added
* [My Setting](../theta-bluetooth-api/shooting_control_command/my_setting.md) : Update new option White Balance Auto Strength
 
### USB-API
* [0xD006 ErrorInfo](../theta-usb-api/property/error_info.md) : Update new error code HIGH_TEMPERATURE_WARNING
* [0xD83A White Balance Auto Strength](../theta-usb-api/property/white_balance_auto_strength.md) : New Added
* [0x99BF GetAccessPointProxy](../theta-usb-api/operation/get_access_point_proxy.md) : New Added
* [0x99C2 GetEthernetProxy](../theta-usb-api/operation/get_ethernet_proxy.md) : New Added
* [0x99C0 SetAccessPointProxy](../theta-usb-api/operation/set_access_point_proxy.md) : New Added
* [0x99C1 SetAccessPointProxyPassword](../theta-usb-api/operation/set_access_point_proxy_password.md) : New Added
* [0x99C3 SetEthernetProxy](../theta-usb-api/operation/set_ethernet_proxy.md) : New Added
* [0x99C4 SetEthernetProxyPassword](../theta-usb-api/operation/set_ethernet_proxy_password.md) : New Added

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
