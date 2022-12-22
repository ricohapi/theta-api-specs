# Options

Options can be acquired by [camera.getOptions](./commands/camera.get_options.md) and set by [camera.setOptions](./commands/camera.set_options.md).

Support value list can be acquired using camera.getOptions with "optionNames" parameter combined the option name and "Support", only if the option corresponds to the acquirement its support value.  
E.g. "iso" support specifications option name: "isoSupport"

Correspondence operation list for each option is as follows.

<table>
  <thead>
    <tr>
      <th>Option Name</th>
      <th>Acquirement</th>
      <th>Setting</th>
      <th>Support Value</th>
      <th>My Settings</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><a href="./options/aperture.md">aperture</a></td>
      <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
      <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
      <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
      <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
    </tr>
    <tr>
      <td><a href="./options/_auto_bracket.md">_autoBracket</a><br />(RICOH THETA S only; firmware version <span class="firmware_version bracket"></span> or later)</td>
      <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
      <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
      <td><img src="./assets/img/partially-supported.png" alt="partially supported" title="partially supported" class="support-mark"></td>
      <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
    </tr>
    <tr>
      <td><a href="./options/_capture_interval.md">_captureInterval</a></td>
      <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
      <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
      <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
      <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
    </tr>
    <tr>
      <td><a href="./options/capture_mode.md">captureMode</a></td>
      <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
      <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
      <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
      <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
    </tr>
    <tr>
      <td><a href="./options/_capture_number.md">_captureNumber</a></td>
      <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
      <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
      <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
      <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
    </tr>
    <tr>
      <td><a href="./options/client_version.md">clientVersion</a><br />(RICOH THETA S firmware version 01.62 or later)</td>
      <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
      <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
      <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
      <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
    </tr>
    <tr>
      <td><a href="./options/_color_temperature.md">_colorTemperature</a><br />(RICOH THETA S only; firmware version 01.82 or later)</td>
      <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
      <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
      <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
      <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    </tr>
    <tr>
      <td><a href="./options/_composite_shooting_output_interval.md">_compositeShootingOutputInterval</a><br />(RICOH THETA S only; firmware version 01.82 or later)</td>
      <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
      <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
      <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
      <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
    </tr>
    <tr>
      <td><a href="./options/_composite_shooting_time.md">_compositeShootingTime</a><br />(RICOH THETA S only; firmware version 01.82 or later)</td>
      <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
      <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
      <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
      <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
    </tr>
    <tr>
      <td><a href="./options/date_time_zone.md">dateTimeZone</a></td>
      <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
      <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
      <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
      <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
    </tr>
    <tr>
      <td><a href="./options/exposure_compensation.md">exposureCompensation</a></td>
      <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
      <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
      <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
      <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    </tr>
    <tr>
    <td><a href="./options/exposure_delay.md">exposureDelay</a><br />(RICOH THETA S firmware version 01.42 or later)</td>
      <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
      <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
      <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
      <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
    </tr>
    <tr>
      <td><a href="./options/exposure_program.md">exposureProgram</a></td>
      <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
      <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
      <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
      <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    </tr>
    <tr>
      <td><a href="./options/file_format.md">fileFormat</a></td>
      <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
      <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
      <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
      <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    </tr>
    <tr>
      <td><a href="./options/_filter.md">_filter</a></td>
      <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
      <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
      <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
      <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    </tr>
    <tr>
      <td><a href="./options/gps_info.md">gpsInfo</a></td>
      <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
      <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
      <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
      <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
    </tr>
    <tr>
      <td><a href="./options/_hdmi_reso.md">_HDMIreso</a></td>
      <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
      <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
      <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
      <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
    </tr>
    <tr>
      <td><a href="./options/iso.md">iso</a></td>
      <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
      <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
      <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
      <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    </tr>
    <tr>
      <td><a href="./options/_latest_enabled_exposure_delay_time.md">_latestEnabledExposureDelayTime</a><br />(RICOH THETA S firmware version 01.42 or later)</td>
      <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
      <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
      <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>     
      <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
    </tr>
    <tr>
      <td><a href="./options/off_delay.md">offDelay</a></td>
      <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
      <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
      <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
      <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
    </tr>
    <tr>
      <td><a href="./options/remaining_pictures.md">remainingPictures</a></td>
      <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
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
    </tr>
    <tr>
      <td><a href="./options/_remaining_videos.md">_remainingVideos</a></td>
      <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
      <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
      <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
      <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
    </tr>
    <tr>
      <td><a href="./options/shutter_speed.md">shutterSpeed</a></td>
      <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
      <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
      <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
      <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
    </tr>
    <tr>
      <td><a href="./options/_shutter_volume.md">_shutterVolume</a></td>
      <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
      <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
      <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
      <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
    </tr>
    <tr>
      <td><a href="./options/sleep_delay.md">sleepDelay</a></td>
      <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
      <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
      <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
      <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
    </tr>
    <tr>
      <td><a href="./options/total_space.md">totalSpace</a></td>
      <td><img src="./assets/img/supported.png" alt="supported" title="supported" class="support-mark"></td>
      <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
      <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
      <td><img src="./assets/img/not-supported.png" alt="not supported" title="not supported" class="support-mark"></td>
    </tr>
    <tr>
      <td><a href="./options/white_balance.md">whiteBalance</a></td>
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
    </tr>
  </tbody>
</table>

![supported](./assets/img/supported.png "supported"): Supported  
![partially supported](./assets/img/partially-supported.png "partially supported"): Partially supported  
![not supported](./assets/img/not-supported.png "not supported"): Not supported  
