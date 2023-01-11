# Property

Camera and shooting properties which can be acquired by [GetDevicePropValue](./operation/get_device_prop_value.md) and set by [SetDevicePropValue](./operation/set_device_prop_value.md).

Use [DevicePropChanged](./event/device_prop_changed.md) to inform of change of device properties. However, change of a property set by [SetDevicePropValue](./operation/set_device_prop_value.md) is not informed.

Supported properties are listed below.

| Property name | Acquisition | Setting |
|:--|:--|:--|
| [0x5001 BatteryLevel](./property/battery_level.md) | ![supported](./assets/img/supported.png "supported") | ![not supported](./assets/img/not-supported.png "not supported") |
| [0x5002 FunctionalMode](./property/functional_mode.md) | ![supported](./assets/img/supported.png "supported") | ![not supported](./assets/img/not-supported.png "not supported") |
| [0x5003 ImageSize](./property/image_size.md) | ![supported](./assets/img/supported.png "supported") | ![supported](./assets/img/supported.png "supported") |
| [0x5005 WhiteBalance](./property/white_balance.md) | ![supported](./assets/img/supported.png "supported") | ![supported](./assets/img/supported.png "supported") |
| [0x5007 F-Number](./property/f_number.md) \*21\*32 | ![supported](./assets/img/supported.png "supported") | ![supported](./assets/img/supported.png "supported") |
| [0x500E ExposureProgramMode](./property/exposure_program_mode.md) | ![supported](./assets/img/supported.png "supported") | ![supported](./assets/img/supported.png "supported") |
| [0x500F ExposureIndex](./property/exposure_index.md) | ![supported](./assets/img/supported.png "supported") | ![supported](./assets/img/supported.png "supported") |
| [0x5010 ExposureBiasCompensation](./property/exposure_bias_compensation.md) | ![supported](./assets/img/supported.png "supported") | ![supported](./assets/img/supported.png "supported") |
| [0x5011 DateTime](./property/date_time.md) | ![supported](./assets/img/supported.png "supported") | ![supported](./assets/img/supported.png "supported") |
| [0x5012 CaptureDelay](./property/capture_delay.md) | ![supported](./assets/img/supported.png "supported") | ![supported](./assets/img/supported.png "supported") |
| [0x5013 StillCaptureMode](./property/still_capture_mode.md) | ![supported](./assets/img/supported.png "supported") | ![supported](./assets/img/supported.png "supported") |
| [0x501A TimelapseNumber](./property/timelapse_number.md) | ![supported](./assets/img/supported.png "supported") | ![supported](./assets/img/supported.png "supported") |
| [0x501B TimelapseInterval](./property/timelapse_interval.md) | ![supported](./assets/img/supported.png "supported") | ![supported](./assets/img/supported.png "supported") |
| [0x502C AudioVolume](./property/audio_volume.md) | ![supported](./assets/img/supported.png "supported") | ![supported](./assets/img/supported.png "supported") |
| [0xD006 ErrorInfo](./property/error_info.md) | ![supported](./assets/img/supported.png "supported") | ![not supported](./assets/img/not-supported.png "not supported") |
| [0xD00F ShutterSpeed](./property/shutter_speed.md) | ![supported](./assets/img/supported.png "supported") | ![supported](./assets/img/supported.png "supported") |
| [0xD407 PerceivedDeviceType](./property/perceived_device_type.md) | ![supported](./assets/img/supported.png "supported") | ![not supported](./assets/img/not-supported.png "not supported") |
| [0xD801 GpsInfo](./property/gps_info.md) | ![supported](./assets/img/supported.png "supported") | ![supported](./assets/img/supported.png "supported") |
| [0xD802 AutoPowerOffDelay](./property/auto_power_off_delay.md) | ![supported](./assets/img/supported.png "supported") | ![supported](./assets/img/supported.png "supported") |
| [0xD803 SleepDelay](./property/sleep_delay.md) | ![supported](./assets/img/supported.png "supported") | ![supported](./assets/img/supported.png "supported") |
| [0xD807 ChannelNumber](./property/channel_number.md) \*01 | ![supported](./assets/img/supported.png "supported") | ![supported](./assets/img/supported.png "supported") |
| [0xD808 CaptureStatus](./property/capture_status.md) | ![supported](./assets/img/supported.png "supported") | ![not supported](./assets/img/not-supported.png "not supported") |
| [0xD809 RecordingTime](./property/recording_time.md) | ![supported](./assets/img/supported.png "supported") | ![not supported](./assets/img/not-supported.png "not supported") |
| [0xD80A RemainingRecordingTime](./property/remaining_recording_time.md) | ![supported](./assets/img/supported.png "supported") | ![not supported](./assets/img/not-supported.png "not supported") |
| [0xD80B Filter](./property/filter.md) | ![supported](./assets/img/supported.png "supported") | ![supported](./assets/img/supported.png "supported") |
| [0xD80C BatteryStatus](./property/battery_status.md) | ![supported](./assets/img/supported.png "supported") | ![not supported](./assets/img/not-supported.png "not supported") |
| [0xD80D RemainingVideos](./property/remaining_videos.md) | ![supported](./assets/img/supported.png "supported") | ![not supported](./assets/img/not-supported.png "not supported") |
| [0xD80E SleepMode](./property/sleep_mode.md) | ![supported](./assets/img/supported.png "supported") | ![supported](./assets/img/supported.png "supported") |
| [0xD80F CompositeShootingTime](./property/composite_shooting_time.md) \*02\*17\*21\*32 | ![supported](./assets/img/supported.png "supported") | ![supported](./assets/img/supported.png "supported") |
| [0xD810 CompositeShootingOutputInterval](./property/composite_shooting_output_interval.md) \*02\*17\*21\*32 | ![supported](./assets/img/supported.png "supported") | ![supported](./assets/img/supported.png "supported") |
| [0xD811 CompositeShootingElapsedTime](./property/composite_shooting_elapsed_time.md) \*02\*17\*21\*32 | ![supported](./assets/img/supported.png "supported") | ![not supported](./assets/img/not-supported.png "not supported") |
| [0xD812 BracketParameters](./property/bracket_parameters.md) \*02 | ![supported](./assets/img/supported.png "supported") | ![supported](./assets/img/supported.png "supported") |
| [0xD813 ColorTemperature](./property/color_temperature.md) \*02 | ![supported](./assets/img/supported.png "supported") | ![supported](./assets/img/supported.png "supported") |
| [0xD814 BluetoothPowerStatus](./property/bluetooth_power_status.md) \*11 | ![supported](./assets/img/supported.png "supported") | ![supported](./assets/img/supported.png "supported") |
| [0xD815 Username](./property/username.md) \*12 | ![supported](./assets/img/supported.png "supported") | ![supported](./assets/img/supported.png "supported") |
| [0xD816 Password](./property/password.md) \*12 | ![supported](./assets/img/supported.png "supported") | ![supported](./assets/img/supported.png "supported") |
| [0xD818 Video Stitching](./property/video_stitching.md) \*11 | ![supported](./assets/img/supported.png "supported") | ![supported](./assets/img/supported.png "supported") |
| [0xD81A MicrophoneChannel](./property/microphone_channel.md) \*11 | ![supported](./assets/img/supported.png "supported") | ![supported](./assets/img/supported.png "supported") |
| [0xD81B AutoPowerOffDelaySec](./property/auto_power_off_delay_sec.md) \*11 | ![supported](./assets/img/supported.png "supported") | ![supported](./assets/img/supported.png "supported") |
| [0xD81C Microphone](./property/microphone.md) \*11\*32 | ![supported](./assets/img/supported.png "supported") | ![supported](./assets/img/supported.png "supported") |
| [0xD81D NetworkType](./property/network_type.md) \*11 | ![supported](./assets/img/supported.png "supported") | ![supported](./assets/img/supported.png "supported") |
| [0xD81F Gain](./property/gain.md) \*11 | ![supported](./assets/img/supported.png "supported") | ![supported](./assets/img/supported.png "supported") |
| [0xD820 Language](./property/language.md) \*11 | ![supported](./assets/img/supported.png "supported") | ![supported](./assets/img/supported.png "supported") |
| [0xD821 Wlan Frequency](./property/wlan_frequency.md) \*11 | ![supported](./assets/img/supported.png "supported") | ![supported](./assets/img/supported.png "supported") |
| [0xD822 CapturedPictures](./property/captured_pictures.md) \*11 | ![supported](./assets/img/supported.png "supported") | ![not supported](./assets/img/not-supported.png "not supported") |
| [0xD823 MaxRecordableTime](./property/max_recordable_time.md) \*11 | ![supported](./assets/img/supported.png "supported") | ![supported](./assets/img/supported.png "supported") |
| [0xD824 Function](./property/function.md) \*21 | ![supported](./assets/img/supported.png "supported") | ![supported](./assets/img/supported.png "supported") |
| [0xD825 TopBottomCorrection](./property/top_bottom_correction.md) \*15 | ![supported](./assets/img/supported.png "supported") | ![supported](./assets/img/supported.png "supported") |
| [0xD826 IsoAutoHighLimit](./property/iso_auto_high_limit.md) \*15 | ![supported](./assets/img/supported.png "supported") | ![supported](./assets/img/supported.png "supported") |
| [0xD827 ImageFormat](./property/image_format.md) \*21 | ![supported](./assets/img/supported.png "supported") | ![supported](./assets/img/supported.png "supported") |
| [0xD829 Bitrate](./property/bitrate.md) \*14 | ![supported](./assets/img/supported.png "supported") | ![supported](./assets/img/supported.png "supported") |
| [0xD82A Authentication](./property/authentication.md) \*15 | ![supported](./assets/img/supported.png "supported") | ![supported](./assets/img/supported.png "supported") |
| [0xD82C BluetoothRole](./property/bluetooth_role.md) \*16\*22\*32 | ![supported](./assets/img/supported.png "supported") | ![supported](./assets/img/supported.png "supported") |
| [0xD831 ConvertVideoFormatStatus](./property/convert_video_format_status.md) \*16\*22 | ![supported](./assets/img/supported.png "supported") | ![not supported](./assets/img/not-supported.png "not supported") |
| [0xD832 GPStagRecording](./property/gps_tag_recording.md) \*31 | ![supported](./assets/img/supported.png "supported") | ![supported](./assets/img/supported.png "supported") |
| [0xD833 TimeShiftParameters](./property/time_shift_parameters.md) \*31 | ![supported](./assets/img/supported.png "supported") | ![supported](./assets/img/supported.png "supported") |
| [0xD834 Image Stitching](./property/image_stitching.md) \*31 | ![supported](./assets/img/supported.png "supported") | ![supported](./assets/img/supported.png "supported") |
| [0xD837 CameraMode](./property/camera_mode.md) \*31 | ![supported](./assets/img/supported.png "supported") | ![supported](./assets/img/supported.png "supported") |
| [0xD839 BurstOption](./property/burst_option.md) \*23 | ![supported](./assets/img/supported.png "supported") | ![supported](./assets/img/supported.png "supported") |
| [0xD83A White Balance Auto Strength](./property/white_balance_auto_strength.md) \*24\*32 | ![supported](./assets/img/supported.png "supported") | ![supported](./assets/img/supported.png "supported") |

![supported](./assets/img/supported.png "supported"): Supported  
![not supported](./assets/img/not-supported.png "not supported"): Not supported  

\*01 Supported by RICOH THETA S and RICOH THETA SC  
\*02 Supported by RICOH THETA S firmware v01.82 or later and RICOH THETA SC firmware v1.10 or later  
\*11 Supported by RICOH THETA V or later  
\*12 Supported by RICOH THETA V firmware v2.00.2 or later  
\*14 Supported by RICOH THETA V firmware v2.50.1 or later  
\*15 Supported by RICOH THETA V firmware v3.00.1 or later  
\*16 Supported by RICOH THETA V firmware v3.21.1 or later  
\*17 RICOH THETA V is not supported  
\*21 Supported by RICOH THETA Z1 or later  
\*22 Supported by RICOH THETA Z1 firmware v1.31.1 or later  
\*23 Supported by RICOH THETA Z1 firmware v2.10.1 or later  
\*24 Supported by RICOH THETA Z1 firmware v2.20.3 or later  
\*31 Supported by RICOH THETA X or later  
\*32 RICOH THETA X is not supported  
