# Options

Camera and shooting properties which can be acquired by [camera.getOptions](./commands/camera.get_options.md) and set by [camera.setOptions](./commands/camera.set_options.md).

For properties available for acquiring supported values, specifying "property name+Support" in the optionNames parameter of camera.getOptions acquires their supported values.   
Example: To acquire the supported values for the "iso" property, specify: "isoSupport"

Supported properties are listed below.

<table>
<thead>
  <tr>
    <th rowspan="2">Option name</th>
    <th rowspan="2">Acquisition</th>
    <th rowspan="2">Setting</th>
    <th rowspan="2">Support Value</th>
    <th class="description_item noborder" colspan="2">My Settings</th>
  </tr>
  <tr>
    <th>Still image <span class="mintext">*01*13</span></th>
    <th>Video <span class="mintext">*13</span></th>
  </tr>
</thead>
<tbody>
  <tr>
    <td><a href="./options/_ai_auto_thumbnail.md">_aiAutoThumbnail</a> <span class="mintext">*31</span></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/partially-supported.png" alt="partially supported" title="partially supported" class="support-mark"> <span class="mintext">*31</span></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
  </tr>
  <tr>
    <td><a href="./options/aperture.md">aperture</a></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"><span class="mintext">*25</span></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/partially-supported.png" alt="partially supported" title="partially supported" class="support-mark"> <span class="mintext">*21</span></td>
    <td><img src="./assets/img/partially-supported.png" alt="partially supported" title="partially supported" class="support-mark"> <span class="mintext">*21</span></td>
  </tr>
  <tr>
    <td><a href="./options/_auto_bracket.md">_autoBracket</a> <span class="mintext">*01</span></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/partially-supported.png" alt="partially supported" title="partially supported" class="support-mark"></td>
    <td><img src="./assets/img/partially-supported.png" alt="partially supported" title="partially supported" class="support-mark"> <span class="mintext">*21</span></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
  </tr>
  <tr>
    <td><a href="./options/_bitrate.md">_bitrate</a> <span class="mintext">*14*21</span></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
  </tr>
  <tr>
    <td><a href="./options/_bluetooth_classic_enable.md">_bluetoothClassicEnable</a> <span class="mintext">*16*23</span></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
  </tr>
  <tr>
    <td><a href="./options/_bluetooth_power.md">_bluetoothPower</a> <span class="mintext">*11</span></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
  </tr>
  <tr>
    <td><a href="./options/_burst_mode.md">_burstMode</a> <span class="mintext">*17*26*32</span></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
  </tr>
  <tr>
    <td><a href="./options/_burst_option.md">_burstOption</a> <span class="mintext">*17*26*32</span></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
    <td><img src="./assets/img/partially-supported.png" alt="partially supported" title="partially supported" class="support-mark"> <span class="mintext">*17*26*32</span></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
  </tr>
  <tr>
    <td><a href="./options/capture_interval.md">captureInterval</a></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/partially-supported.png" alt="partially supported" title="partially supported" class="support-mark"> <span class="mintext">*21</span></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
  </tr>
  <tr>
    <td><a href="./options/capture_mode.md">captureMode</a></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
  </tr>
  <tr>
    <td><a href="./options/_camera_mode.md">_cameraMode</a> <span class="mintext">*31</span></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
  </tr>
  <tr>
    <td><a href="./options/_camera_control_source.md">_cameraControlSource</a> <span class="mintext">*31</span></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
  </tr>
  <tr>
    <td><a href="./options/capture_number.md">captureNumber</a></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/partially-supported.png" alt="partially supported" title="partially supported" class="support-mark"> <span class="mintext">*21</span></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
  </tr>
  <tr>
    <td><a href="./options/client_version.md">clientVersion</a></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
  </tr>
  <tr>
    <td><a href="./options/_color_temperature.md">_colorTemperature</a> <span class="mintext">*01</span></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
  </tr>
  <tr>
    <td><a href="./options/_composite_shooting_output_interval.md">_compositeShootingOutputInterval</a> <span class="mintext">*01*17*32</span></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/partially-supported.png" alt="partially supported" title="partially supported" class="support-mark"> <span class="mintext">*21</span></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
  </tr>
  <tr>
    <td><a href="./options/_composite_shooting_time.md">_compositeShootingTime</a> <span class="mintext">*01*17*32</span></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/partially-supported.png" alt="partially supported" title="partially supported" class="support-mark"> <span class="mintext">*21</span></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
  </tr>
  <tr>
    <td><a href="./options/continuous_number.md">continuousNumber</a> <span class="mintext">*31</span></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
  </tr>
  <tr>
    <td><a href="./options/date_time_zone.md">dateTimeZone</a></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
  </tr>
  <tr>
    <td><a href="./options/exposure_compensation.md">exposureCompensation</a></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
  </tr>
  <tr>
  <td><a href="./options/exposure_delay.md">exposureDelay</a></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/partially-supported.png" alt="partially supported" title="partially supported" class="support-mark"> <span class="mintext">*15</span></td>
    <td><img src="./assets/img/partially-supported.png" alt="partially supported" title="partially supported" class="support-mark"> <span class="mintext">*15</span></td>
  </tr>
  <tr>
    <td><a href="./options/exposure_program.md">exposureProgram</a></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/partially-supported.png" alt="partially supported" title="partially supported" class="support-mark"> <span class="mintext">*15</span></td>
  </tr>
  <tr>
    <td><a href="./options/_face_detect.md">_faceDetect</a> <span class="mintext">*31</span></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/partially-supported.png" alt="partially supported" title="partially supported" class="support-mark"> <span class="mintext">*31</span></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
  </tr>
  <tr>
    <td><a href="./options/file_format.md">fileFormat</a></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/partially-supported.png" alt="partially supported" title="partially supported" class="support-mark"> <span class="mintext">*01*15</span></td>
    <td><img src="./assets/img/partially-supported.png" alt="partially supported" title="partially supported" class="support-mark"> <span class="mintext">*15</span></td>
  </tr>
  <tr>
    <td><a href="./options/_filter.md">_filter</a></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
  </tr>
  <tr>
    <td><a href="./options/_function.md">_function</a> <span class="mintext">*21</span></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
  </tr>
  <tr>
    <td><a href="./options/_gain.md">_gain</a> <span class="mintext">*11</span></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
  </tr>
  <tr>
    <td><a href="./options/gps_info.md">gpsInfo</a></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
  </tr>
  <tr>
    <td><a href="./options/_gps_tag_recording.md">_gpsTagRecording</a> <span class="mintext">*31</span></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
  </tr>
  <tr>
    <td><a href="./options/_hdmi_reso.md">_HDMIreso</a> <span class="mintext">*17*24*32</span></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
  </tr>
  <tr>
    <td><a href="./options/_image_stitching.md">_imageStitching</a> <span class="mintext">*15</span></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
  </tr>
  <tr>
    <td><a href="./options/iso.md">iso</a></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/partially-supported.png" alt="partially supported" title="partially supported" class="support-mark"> <span class="mintext">*15</span></td>
  </tr>
  <tr>
    <td><a href="./options/iso_auto_high_limit.md">isoAutoHighLimit</a> <span class="mintext">*15</span></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/partially-supported.png" alt="partially supported" title="partially supported" class="support-mark"> <span class="mintext">*15</span></td>
    <td><img src="./assets/img/partially-supported.png" alt="partially supported" title="partially supported" class="support-mark"> <span class="mintext">*15</span></td>
  </tr>
  <tr>
  <td><a href="./options/_language.md">_language</a> <span class="mintext">*11</span></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
  </tr>
  <tr>
  <td><a href="./options/_latest_enabled_exposure_delay_time.md">_latestEnabledExposureDelayTime</a></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>     
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
  </tr>
  <tr>
    <td><a href="./options/_max_recordable_time.md">_maxRecordableTime</a> <span class="mintext">*11</span></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
    <td><img src="./assets/img/partially-supported.png" alt="partially supported" title="partially supported" class="support-mark"> <span class="mintext">*15</span></td>
  </tr>
  <tr>
    <td><a href="./options/_microphone.md">_microphone</a> <span class="mintext">*11</span></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
  </tr>
  <tr>
    <td><a href="./options/_microphone_channel.md">_microphoneChannel</a> <span class="mintext">*11</span></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
  </tr>
  <tr>
    <td><a href="./options/_network_type.md">_networkType</a> <span class="mintext">*11</span></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
  </tr>
  <tr>
    <td><a href="./options/off_delay.md">offDelay</a></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
  </tr>
  <tr>
    <td><a href="./options/_power_saving.md">_powerSaving</a> <span class="mintext">*31</span></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
  </tr>
  <tr>
    <td><a href="./options/_password.md">_password</a> <span class="mintext">*12</span></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
  </tr>
  <tr>
    <td><a href="./options/preview_format.md">previewFormat</a></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
  </tr>
  <tr>
    <td><a href="./options/remaining_pictures.md">remainingPictures</a></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
  </tr>
  <tr>
    <td><a href="./options/remaining_space.md">remainingSpace</a></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
  </tr>
  <tr>
    <td><a href="./options/remaining_video_seconds.md">remainingVideoSeconds</a></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
  </tr>
  <tr>
    <td><a href="./options/_shooting_method.md">_shootingMethod</a> <span class="mintext">*21</span></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/partially-supported.png" alt="partially supported" title="partially supported" class="support-mark"> <span class="mintext">*21</span></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
  </tr>
  <tr>
    <td><a href="./options/shutter_speed.md">shutterSpeed</a></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/partially-supported.png" alt="partially supported" title="partially supported" class="support-mark"> <span class="mintext">*15</span></td>
  </tr>
  <tr>
    <td><a href="./options/_shutter_volume.md">_shutterVolume</a></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
  </tr>
  <tr>
    <td><a href="./options/sleep_delay.md">sleepDelay</a></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
  </tr>
  <tr>
    <td><a href="./options/_time_shift.md">_timeShift</a> <span class="mintext">*15</span></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
  </tr>
  <tr>
    <td><a href="./options/_top_bottom_correction.md">_topBottomCorrection</a> <span class="mintext">*15</span></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
  </tr>
  <tr>
    <td><a href="./options/_top_bottom_correction_rotation.md">_topBottomCorrectionRotation</a> <span class="mintext">*33</span></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
  </tr>
  <tr>
    <td><a href="./options/total_space.md">totalSpace</a></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
  </tr>
  <tr>
    <td><a href="./options/_username.md">_username</a> <span class="mintext">*12</span></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
  </tr>
  <tr>
    <td><a href="./options/video_stitching.md">videoStitching</a> <span class="mintext">*11</span></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
  </tr>
  <tr>
    <td><a href="./options/_visibility_reduction.md">_visibilityReduction</a> <span class="mintext">*22</span></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
  </tr>
  <tr>
    <td><a href="./options/white_balance.md">whiteBalance</a></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
  </tr>
  <tr>
    <td><a href="./options/_white_balance_auto_strength.md">_whiteBalanceAutoStrength</a> <span class="mintext">*27</span></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
  </tr>
  <tr>
    <td><a href="./options/_wlan_channel.md">_wlanChannel</a></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
   <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
  </tr>
  <tr>
    <td><a href="./options/_wlan_frequency.md">_wlanFrequency</a> <span class="mintext">*11</span></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
    <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
  </tr>
</tbody>
</table>

![supported](./assets/img/supported.png "supported"): Supported  
![partially supported](./assets/img/partially-supported.png "partially supported"): Partially supported  
![not supported](./assets/img/not-supported.png "not supported"): Not supported  

\*01 RICOH THETA S firmware v01.82 or later and RICOH THETA SC firmware v1.10 or later  
\*11 RICOH THETA V or later  
\*12 RICOH THETA V firmware v2.00.2 or later  
\*13 RICOH THETA V firmware v2.30.1 or later  
\*14 RICOH THETA V firmware v2.50.1 or later  
\*15 RICOH THETA V firmware v3.00.1 or later  
\*16 RICOH THETA V firmware v3.40.1 or later  
\*17 RICOH THETA V is not supported  
\*21 RICOH THETA Z1 or later  
\*22 RICOH THETA Z1 firmware v1.11.1 or later  
\*23 RICOH THETA Z1 firmware v1.50.1 or later  
\*24 RICOH THETA Z1 is not supported  
\*25 RICOH THETA Z1 only    
\*26 RICOH THETA Z1 firmware v2.10.1 or later  
\*27 RICOH THETA Z1 firmware v2.20.3 or later  
\*31 RICOH THETA X or later  
\*32 RICOH THETA X is not supported  
\*33 RICOH THETA X firmware v1.20.0 or later  
