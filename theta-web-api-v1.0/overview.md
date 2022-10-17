# Overview

Obtain the prerequisite specifications from below.

- [PTP Specification (v.1.1)](https://www.iso.org/iso/home/store/catalogue_ics/catalogue_detail_ics.htm?csnumber=45344)
- [PTP-IP Specification (v.1.0)](https://www.cipa.jp/ptp-ip/contents_e/01guide_e.html)

### PTP-IP Packet

The RICOH THETA support status for PTP-IP packets is as follows

| Name | RICOH THETA Specification |
|:--|:--|
| Init Command Request | support |
| Init Command Ack | support |
| Init Event Request | support |
| Init Event Ack | support |
| Init Fail | support |
| Operation Request | support |
| Operation Response | support |
| Event | support |
| Start Data | support |
| Data | support |
| Cancel | non-support |
| End Data | support |
| Probe Request | support (I→R only) |
| Probe Response | support (R→I only) |

\*　I: Initiator  
\*　R: Responder

### Operations

<dl>
  <dt><a href="operation/get_device_info.md">0x1001 GetDeviceInfo</a></dt>
  <dd>Return device information data.</dd>
</dl>
<dl>
  <dt><a href="operation/open_session.md">0x1002 OpenSession</a></dt>
  <dd>Open a session.</dd>
</dl>
<dl>
  <dt><a href="operation/close_session.md">0x1003 CloseSession</a></dt>
  <dd>Close the session.</dd>
</dl>
<dl>
  <dt><a href="operation/get_storageids.md">0x1004 GetStorageIDs</a></dt>
  <dd>Return the current valid storage ID list.</dd>
</dl>
<dl>
  <dt><a href="operation/get_storage_info.md">0x1005 GetStorageInfo</a></dt>
  <dd>Return information on the specified storage ID.</dd>
</dl>
<dl>
  <dt><a href="operation/get_num_objects.md">0x1006 GetNumObjects</a></dt>
  <dd>Return the number of objects for the specified storage ID.</dd>
</dl>
<dl>
  <dt><a href="operation/get_object_handles.md">0x1007 GetObjectHandles</a></dt>
  <dd>Return the ObjectHandle for the specified storage ID.</dd>
</dl>
<dl>
  <dt><a href="operation/get_object_info.md">0x1008 GetObjectInfo</a></dt>
  <dd>Return object information for the specified ObjectHandle.</dd>
</dl>
<dl>
  <dt><a href="operation/get_object.md">0x1009 GetObject</a></dt>
  <dd>Return the object for the specified ObjectHandle.</dd>
</dl>
<dl>
  <dt><a href="operation/get_thumb.md">0x100A GetThumb</a></dt>
  <dd>Return the thumbnail within the specified ObjectHandle.</dd>
</dl>
<dl>
  <dt><a href="operation/delete_object.md">0x100B DeleteObject</a></dt>
  <dd>Delete the object for the specified ObjectHandle.</dd>
</dl>
<dl>
  <dt><a href="operation/initiate_capture.md">0x100E InitiateCapture</a></dt>
  <dd>Start shooting.</dd>
</dl>
<dl>
  <dt><a href="operation/get_device_prop_desc.md">0x1014 GetDevicePropDesc</a></dt>
  <dd>Return the Device Property Description for the specified Device Property.</dd>
</dl>
<dl>
  <dt><a href="operation/get_device_prop_value.md">0x1015 GetDevicePropValue</a></dt>
  <dd>Return the Device Property value for the specified Device Property.</dd>
</dl>
<dl>
  <dt><a href="operation/set_device_prop_value.md">0x1016 SetDevicePropValue</a></dt>
  <dd>Set the current value for the specified Device Property.</dd>
</dl>
<dl>
  <dt><a href="operation/terminate_open_capture.md">0x1018 TerminateOpenCapture</a></dt>
  <dd>Exit continuous shooting for the specified TransactionID.</dd>
</dl>
<dl>
  <dt><a href="operation/initiate_open_capture.md">0x101C InitiateOpenCapture</a></dt>
  <dd>Start capture. Video (RICOH THETA m15) and interval.</dd>
</dl>
<dl>
  <dt><a href="operation/get_resized_image_object.md">0x1022 GetResizedImageObject</a></dt>
  <dd>An object resized to 2048 x 1024 pixels is acquired for the specified object handle.</dd>
</dl>
<dl>
  <dt><a href="operation/wlan_power_control.md">0x99A1 WlanPowerControl</a></dt>
  <dd>Turns Wireless LAN OFF.</dd>
</dl>

### Properties

<dl>
  <dt><a href="property/battery_level.md">0x5001 BatteryLevel</a></dt>
  <dd>Acquire the charge level.</dd>
</dl>
<dl>
  <dt><a href="property/white_balance.md">0x5005 WhiteBalance</a></dt>
  <dd>Acquire or set the white balance.</dd>
</dl>
<dl>
  <dt><a href="property/exposure_index.md">0x500F ExposureIndex</a></dt>
  <dd>Acquire or set the ISO sensitivity.</dd>
</dl>
<dl>
  <dt><a href="property/exposure_bias_compensation.md">0x5010 ExposureBiasCompensation</a></dt>
  <dd>Acquire or set the exposure compensation value.</dd>
</dl>
<dl>
  <dt><a href="property/date_time.md">0x5011 DateTime</a></dt>
  <dd>Acquire or set the date and time.</dd>
</dl>
<dl>
  <dt><a href="property/still_capture_mode.md">0x5013 StillCaptureMode</a></dt>
  <dd>Acquire or set the still image shooting method.</dd>
</dl>
<dl>
  <dt><a href="property/timelapse_number.md">0x501A TimelapseNumber</a></dt>
  <dd>Acquire or set the upper limit value for interval shooting.</dd>
</dl>
<dl>
  <dt><a href="property/timelapse_interval.md">0x501B TimelapseInterval</a></dt>
  <dd>Acquire or set the shooting interval (msec) for interval shooting.</dd>
</dl>
<dl>
  <dt><a href="property/audio_volume.md">0x502C AudioVolume</a></dt>
  <dd>Acquire or set the volume for the shutter sound.</dd>
</dl>
<dl>
  <dt><a href="property/error_info.md">0xD006 ErrorInfo</a></dt>
  <dd>Acquire error information.</dd>
</dl>
<dl>
  <dt><a href="property/shutter_speed.md">0xD00F ShutterSpeed</a></dt>
  <dd>Acquire or set the shutter speed.</dd>
</dl>
<dl>
  <dt><a href="property/gps_info.md">0xD801 GpsInfo</a></dt>
  <dd>Acquire or set the GPS information.</dd>
</dl>
<dl>
  <dt><a href="property/auto_power_off_delay.md">0xD802 AutoPowerOffDelay</a></dt>
  <dd>Acquire or set auto power off for the camera (minutes).</dd>
</dl>
<dl>
  <dt><a href="property/sleep_delay.md">0xD803 SleepDelay</a></dt>
  <dd>Acquire or set the camera sleep mode (seconds).</dd>
</dl>
<dl>
  <dt><a href="property/channel_number.md">0xD807 ChannelNumber </a></dt>
  <dd>Acquire or set the wireless LAN channel.</dd>
</dl>
<dl>
  <dt><a href="property/capture_status.md">0xD808 CaptureStatus</a></dt>
  <dd>Acquire the camera shooting execution status.</dd>
</dl>
<dl>
  <dt><a href="property/recording_time.md">0xD809 RecordingTime</a></dt>
  <dd>Acquire the video recording time (seconds). (RICOH THETA m15)</dd>
</dl>
<dl>
  <dt><a href="property/remaining_recording_time.md">0xD80A RemainingRecordingTime</a></dt>
  <dd>Acquire the amount of time remaining (seconds) for shooting video. (RICOH THETA m15)</dd>
</dl>

### Events

<dl>
  <dt><a href="event/object_added.md">0x4002 ObjectAdded</a></dt>
  <dd>Notification of an object addition.</dd>
</dl>
<dl>
  <dt><a href="event/device_prop_changed.md">0x4006 DevicePropChanged</a></dt>
  <dd>Notification of a Device Property change.</dd>
</dl>
<dl>
  <dt><a href="event/store_full.md">0x400A StoreFull</a></dt>
  <dd>Storage FULL notification.</dd>
</dl>
<dl>
  <dt><a href="event/capture_complete.md">0x400D CaptureComplete</a></dt>
  <dd>Notifies that shooting is finished.</dd>
</dl>
