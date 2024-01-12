# Camera API

RICOH THETA V and Z1 support android.hardware.Camera package to controll 360 camera. Plugin app need to send specified broadcast intent to use camera resource. Refer to [Notifying Camera Device Control](broadcast-intent.md/#notifying-camera-device-control) for detail.
RICOH THETA V and Z1 do not support android.hardware.camera2 package, by the way.

RICOH THETA X support com.theta360.hardware.Camera package to controll 360 camera. Plugin app need to import these packages via [THETA Plugin Library](https://github.com/ricohapi/theta-plugin-library).  

Followings are sample projects of RICOH THETA Plugin to controll camera feature by plugin via Camera API.
* [THETA Plugin: CameraAPI Sample](https://github.com/ricohapi/theta-plugin-camera-api-sample) for THETA V/Z1/X.
* [THETA X Plugin : Camera API Sample](https://github.com/ricohapi/theta-plugin-camera-api-sample-x) for THETA X.

RICOH THETA V, Z1, and X define original parameters as listed below. They can be set via Camera.Parameters.set API.

### Contents

* [Shooting Mode](#shooting-mode)
* [Stitching](#stitching)
* [Zenith Correction](#zenith-correction)
* [Exposure Program](#exposure-program)
* [Auto Exposure Lock](#auto-exposure-lock)
* [Shutter Speed](#shutter-speed)
* [ISO Sensitivity](#iso-sensitivity)
* [ISO Sensitivity Upper Limit](#iso-sensitivity-upper-limit)
* [Aperture](#aperture)
* [White Balance](#white-balance)
* [Color Temperature](#color-temperature)
* [White Balance Auto Strength](#white-balance-auto-strength)
* [Exposure Compensation](#exposure-compensation)
* [Activate Image File Size Specification](#activate-image-file-size-specification)
* [Image File Size](#image-file-size)
* [Switching DNG Output](#switching-dng-output)
* [Burst Capture Mode](#burst-capture-mode)
* [Face Detection](#face-detection)

## Shooting Mode
To set shooting mode, set value (String type) for "RIC_SHOOTING_MODE". 

### RICOH THETA V, Z1

<table>
    <thead>
      <tr>
        <th width="40%">Value</th>
        <th width="60%">Description</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>"RicMonitoring"</td>
        <td>Monitoring (Z1 can use this mode for normal Still Image Shooting only, cannot use it for HDR, HhHDR, and NR mode.)</td>
      </tr>
      <tr>
        <td>"RicMoviePreview640"</td>
        <td>Live View (640x320)</td>
      </tr>
      <tr>
        <td>"RicMoviePreview1024"</td>
        <td>Live View (1024x512)</td>
      </tr>
      <tr>
        <td>"RicMoviePreview1920"</td>
        <td>Live View (1920x960)</td>
      </tr>
      <tr>
        <td>"RicMoviePreview3840"</td>
        <td>Live View (3840x1920)</td>
      </tr>
      <tr>
        <td>"RicStillCaptureStd"</td>
        <td>Still Image Shooting</td>
      </tr>
      <tr>
        <td>"RicStillCaptureStdBurst"</td>
        <td>Still Image Shooting (Burst Capture Mode)<br>(RICOH THETA Z1 firmware v2.00.1 or later)</td>
      </tr>
      <tr>
        <td>"RicStillCaptureWDR"</td>
        <td>DR Correction</td>
      </tr>
      <tr>
        <td>"RicStillCaptureMultiRawNR"</td>
        <td>Noise Reduction</td>
      </tr>
      <tr>
        <td>"RicStillCaptureMultiYuvHdr"</td>
        <td>HDR Rendering</td>
      </tr>
      <tr>
        <td>"RicStillCaptureMultiYuvHhHdr"</td>
        <td>Handheld HDR Rendering<br>(RICOH THETA Z1 firmware v1.20.1 or later and RICOH THETA V firmware v3.10.1 or later)</td>
      </tr>
      <tr>
        <td>"RicMovieRecording4kEqui"</td>
        <td>Equirectangular Formatted Movie (3840x1920)</td>
      </tr>
      <tr>
        <td>"RicMovieRecording4kDual"</td>
        <td>Dual-Fisheye Formatted Movie (3840x1920)</td>
      </tr>
      <tr>
        <td>"RicMovieRecording2kEqui"</td>
        <td>Equirectangular Formatted Movie (1920x960)</td>
      </tr>
      <tr>
        <td>"RicMovieRecording2kDual"</td>
        <td>Dual-Fisheye Formatted Movie (1920x960)</td>
      </tr>
    </tbody>
  </table>  

### RICOH THETA X

<table>
    <thead>
      <tr>
        <th width="40%">Value</th>
        <th width="60%">Description</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>"RicPreview1024"</td>
        <td>Live View (1024x512)</td>
      </tr>
      <tr>
        <td>"RicPreview1920"</td>
        <td>Live View (1920x960)</td>
      </tr>
      <tr>
        <td>"RicPreview3840"</td>
        <td>Live View (3840x1920)</td>
      </tr>
      <tr>
        <td>"RicPreview5760"</td>
        <td>Live View (5760x2880)</td>
      </tr>
      <tr>
        <td>"RicPreview1024:576"</td>
        <td>Live View (1024x576)</td>
      </tr>
      <tr>
        <td>"RicPreview1920:1080"</td>
        <td>Live View (1920×1080)</td>
      </tr>
      <tr>
        <td>"RicPreview3840:2160"</td>
        <td>Live View (3840x2160)</td>
      </tr>
      <tr>
        <td>"RicStillCaptureStd"</td>
        <td>Still Image Shooting</td>
      </tr>
      <tr>
        <td>"RicStillCaptureMultiRawNR"</td>
        <td>Noise Reduction</td>
      </tr>
      <tr>
        <td>"RicStillCaptureMultiYuvHdr"</td>
        <td>HDR Rendering</td>
      </tr>
      <tr>
        <td>"RicStillCaptureMultiYuvHhHdr"</td>
        <td>Handheld HDR Rendering<br>RICOH THETA X firmware v2.40.0 or later</td>
      </tr>
      <tr>
        <td>"RicMovieRecording1920"</td>
        <td>2K video</td>
      </tr>
      <tr>
        <td>"RicMovieRecording3840"</td>
        <td>4K video</td>
      </tr>
      <tr>
        <td>"RicMovieRecording5760"</td>
        <td>5.7K video</td>
      </tr>
      <tr>
        <td>"RicMovieRecording7680"</td>
        <td>8K video<br>8K video mode is available up to 10fps. Plugin app need to set video fps like setVideoFrameRate(10).<br>8K video can be encoded with I-frame only configuration. Plugin app need to set I-frame interval like setVideoEncodingIFrameInterval(0.0f).</td>
      </tr>
    </tbody>
  </table>  

## Stitching
To set stitching, set the value (String type) for "RIC_PROC_STITCHING".

<table>
    <thead>
      <tr>
        <th width="40%">Value</th>
        <th width="60%">Description</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>"RicNonStitching"</td>
        <td>For Dual Fish Eye Image</td>
      </tr>
      <tr>
        <td>"RicStaticStitching"</td>
        <td>For Static Stitching</td>
      </tr>
      <tr>
        <td>"RicDynamicStitchingAuto"</td>
        <td>For Dynamic Stitching</td>
      </tr>
    </tbody>
  </table>  

To optimize stitching process with using water housing TW-2, set the value (int type) for "RIC_WATER_HOUSING". This is available for RICOH THETA X firmware v1.40.0 or later.

<table>
  <thead>
    <tr>
      <th width="40%">Value</th>
      <th width="60%">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>0</td>
      <td>not use TW-2</td>
    </tr>
    <tr>
      <td>1</td>
      <td>use TW-2 in underwater</td>
    </tr>
    <tr>
      <td>2</td>
      <td>use TW-2 on land</td>
  </tr>
  </tbody>
</table>

## Zenith Correction

Set the zenith correction method using "RIC_PROC_ZENITH_CORRECTION".
To set zenith correction, set the value (String type) for "RIC_PROC_ZENITH_CORRECTION".  
“RIC_ZENITH_DIRECTION” passes the rotation pitch/roll/yaw. (RICOH THETA X only)
The format of RIC_ZENITH_DIRECTION is "%.02f_%.02f_%.02f" as String. For example, "15.0_30.0_45.0" means that pitch=15.0deg, roll=30.0deg, and yaw=45.0deg".

<table>
    <thead>
      <tr>
        <th width="40%">Value</th>
        <th width="60%">Description</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>"RicZenithCorrectionOff"</td>
        <td>Off</td>
      </tr>
      <tr>
        <td>"RicZenithCorrectionOnAuto"</td>
        <td>Auto Zenith Correction (*1)</td>
      </tr>
      <tr>
        <td>"RicZenithCorrectionOnManual"</td>
        <td>Fixed Parameters (RICOH THETA X only)</td>
      </tr>
    </tbody>
  </table>  

(*1) THETA V and Z1 must send this [Broadcast Intent](./broadcast-intent.md#control-imu-sensor) to start IMU sensor, before capturing via Camera API.

## Exposure Program
To set the exposure program, set the value (String type) for "RIC_EXPOSURE_MODE".

|Value|Description|
|:-|:-|
|"RicManualExposure"|Manual Exposure Mode for normal|
|"RicAutoExposureP"|Program Auto Exposure Mode|
|"RicAutoExposureA"|Av priority Auto Exposure mode. Iris setting (RICOH THETA Z1 only)|
|"RicAutoExposureT"|Tv Priority Auto Exposure Mode. Exposure time|
|"RicAutoExposureS"|Sv Priority Auto Exposure Mode, Exposure gain|

## Auto Exposure Lock

Set “RIC_EXPOSURE_LOCK” to lock the auto-exposure routine.

<table>
    <thead>
      <tr>
        <th width="20%">Value</th>
        <th width="80%">Description</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>0</td>
        <td>unlocked</td>
      </tr>
      <tr>
        <td>1</td>
        <td>locked</td>
      </tr>
    </tbody>
  </table> 

## Shutter Speed
To set shutter speed, set the values (int type) for "RIC_MANUAL_EXPOSURE_TIME_FRONT" and "RIC_MANUAL_EXPOSURE_TIME_REAR". When "RIC_EXPOSURE_MODE" is "RicManualExposure", longer than 1/8 sec can be set. When "RIC_EXPOSURE_MODE" is "RicAutoExposureT", from 1/25000 to 15 \* can be set. When "RIC_EXPOSURE_MODE" is "RicAutoExposureP", "RicAutoExposureA", "RicAutoExposureS", or "RicAutoExposureWDR", only AUTO can be set. It is recommended that the same value be set for "RIC_MANUAL_EXPOSURE_TIME_FRONT" and "RIC_MANUAL_EXPOSURE_TIME_REAR". There is no guarantee of the action if different values are set. 

\* For RICOH THETA Z1 firmware v1.50.1 or earlier and RICOH THETA V firmware v3.40.1 or earlier, from 1/25000 to 1/8 can be set.

<table>
    <thead>
      <tr>
        <th width="20%">Value</th>
        <th width="80%">Description</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>-1</td>
        <td>Auto</td>
      </tr>
      <tr>
        <td>0</td>
        <td>1/25000 sec (RICOH THETA X is not supported)</td>
      </tr>
      <tr>
        <td>1</td>
        <td>1/20000 sec (RICOH THETA X is not supported)</td>
      </tr>
      <tr>
        <td>2</td>
        <td>1/16000 sec</td>
      </tr>
      <tr>
        <td>3</td>
        <td>1/12500 sec (RICOH THETA V, Z1)<br>1/12800 sec (RICOH THETA X)</td>
      </tr>
      <tr>
        <td>4</td>
        <td>1/10000 sec</td>
      </tr>
      <tr>
        <td>5</td>
        <td>1/8000 sec</td>
      </tr>
      <tr>
        <td>6</td>
        <td>1/6400 sec</td>
      </tr>
      <tr>
        <td>7</td>
        <td>1/5000 sec</td>
      </tr>
      <tr>
        <td>8</td>
        <td>1/4000 sec</td>
      </tr>
      <tr>
        <td>9</td>
        <td>1/3200 sec</td>
      </tr>
      <tr>
        <td>10</td>
        <td>1/2500 sec</td>
      </tr>
      <tr>
        <td>11</td>
        <td>1/2000 sec</td>
      </tr>
      <tr>
        <td>12</td>
        <td>1/1600 sec</td>
      </tr>
      <tr>
        <td>13</td>
        <td>1/1250 sec</td>
      </tr>
      <tr>
        <td>14</td>
        <td>1/1000 sec</td>
      </tr>
      <tr>
        <td>15</td>
        <td>1/800 sec</td>
      </tr>
      <tr>
        <td>16</td>
        <td>1/640 sec</td>
      </tr>
      <tr>
        <td>17</td>
        <td>1/500 sec</td>
      </tr>
      <tr>
        <td>18</td>
        <td>1/400 sec</td>
      </tr>
      <tr>
        <td>19</td>
        <td>1/320 sec</td>
      </tr>
      <tr>
        <td>20</td>
        <td>1/250 sec</td>
      </tr>
      <tr>
        <td>21</td>
        <td>1/200 sec</td>
      </tr>
      <tr>
        <td>22</td>
        <td>1/160 sec</td>
      </tr>
      <tr>
        <td>23</td>
        <td>1/125 sec</td>
      </tr>
      <tr>
        <td>24</td>
        <td>1/100 sec</td>
      </tr>
      <tr>
        <td>25</td>
        <td>1/80 sec</td>
      </tr>
      <tr>
        <td>26</td>
        <td>1/60 sec</td>
      </tr>
      <tr>
        <td>27</td>
        <td>1/50 sec</td>
      </tr>
      <tr>
        <td>28</td>
        <td>1/40 sec</td>
      </tr>
      <tr>
        <td>29</td>
        <td>1/30 sec</td>
      </tr>
      <tr>
        <td>30</td>
        <td>1/25 sec</td>
      </tr>
      <tr>
        <td>31</td>
        <td>1/20 sec</td>
      </tr>
      <tr>
        <td>32</td>
        <td>1/15 sec</td>
      </tr>
      <tr>
        <td>33</td>
        <td>1/13 sec</td>
      </tr>
      <tr>
        <td>34</td>
        <td>1/10 sec</td>
      </tr>
      <tr>
        <td>35</td>
        <td>1/8 sec</td>
      </tr>
      <tr>
        <td>36</td>
        <td>1/6 sec</td>
      </tr>
      <tr>
        <td>37</td>
        <td>1/5 sec</td>
      </tr>
      <tr>
        <td>38</td>
        <td>1/4 sec</td>
      </tr>
      <tr>
        <td>39</td>
        <td>1/3 sec</td>
      </tr>
      <tr>
        <td>40</td>
        <td>1/2.5 sec</td>
      </tr>
      <tr>
        <td>41</td>
        <td>1/2 sec</td>
      </tr>
      <tr>
        <td>42</td>
        <td>1/1.6 sec</td>
      </tr>
      <tr>
        <td>43</td>
        <td>1/1.3 sec</td>
      </tr>
      <tr>
        <td>44</td>
        <td>1 sec</td>
      </tr>
      <tr>
        <td>45</td>
        <td>1.3 sec</td>
      </tr>
      <tr>
        <td>46</td>
        <td>1.6 sec</td>
      </tr>
      <tr>
        <td>47</td>
        <td>2 sec</td>
      </tr>
      <tr>
        <td>48</td>
        <td>2.5 sec</td>
      </tr>
      <tr>
        <td>49</td>
        <td>3.2 sec</td>
      </tr>
      <tr>
        <td>50</td>
        <td>4 sec</td>
      </tr>
      <tr>
        <td>51</td>
        <td>5 sec</td>
      </tr>
      <tr>
        <td>52</td>
        <td>6 sec</td>
      </tr>
      <tr>
        <td>53</td>
        <td>8 sec</td>
      </tr>
      <tr>
        <td>54</td>
        <td>10 sec</td>
      </tr>
      <tr>
        <td>55</td>
        <td>13 sec</td>
      </tr>
      <tr>
        <td>56</td>
        <td>15 sec</td>
      </tr>
      <tr>
        <td>57</td>
        <td>20 sec</td>
      </tr>
      <tr>
        <td>58</td>
        <td>25 sec</td>
      </tr>
      <tr>
        <td>59</td>
        <td>30 sec</td>
      </tr>
      <tr>
        <td>60</td>
        <td>40 sec (RICOH THETA X only)</td>
      </tr>
      <tr>
        <td>61</td>
        <td>50 sec (RICOH THETA X only)</td>
      </tr>
      <tr>
        <td>62</td>
        <td>60 sec</td>
      </tr>
    </tbody>
  </table> 


## ISO Sensitivity
To set ISO sensitivity, set the value (int type) for "RIC_MANUAL_EXPOSURE_ISO_FRONT" and "RIC_MANUAL_EXPOSURE_ISO_REAR". When "RIC_EXPOSURE_MODE" is "RicAutoExposureP", "RicAutoExposureA", "RicAutoExposureT", or "RicAutoExposureWDR", only AUTO can be set. It is recommended that the same value be set for "RIC_MANUAL_EXPOSURE_ISO_FRONT" and "RIC_MANUAL_EXPOSURE_ISO_REAR". There is no guarantee of the action if different values are set. 

When the model of the camera is RICOH THETA V, in image shooting mode, a value of 64 to 3200 can be set.
When the model of the camera is RICOH THETA V, in video recording mode, a value of 64 to 6400 can be set. 
When the model of the camera is RICOH THETA Z1, in image shooting mode or video recording mode, a value of 80 to 6400 can be set.
When the model of the camera is RICOH THETA X, in image shooting mode or video recording mode, a value of 50 to 3200 can be set.

<table>
    <thead>
      <tr>
        <th width="20%">Value</th>
        <th width="80%">Description</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>-1</td>
        <td>Auto</td>
      </tr>
      <tr>
        <td>0</td>
        <td>50 (RICOH THETA X only)</td>
      </tr>
      <tr>
        <td>1</td>
        <td>64 (RICOH THETA Z1 is not supported)</td>
      </tr>
      <tr>
        <td>2</td>
        <td>80</td>
      </tr>
      <tr>
        <td>3</td>
        <td>100</td>
      </tr>
      <tr>
        <td>4</td>
        <td>125</td>
      </tr>
      <tr>
        <td>5</td>
        <td>160</td>
      </tr>
      <tr>
        <td>6</td>
        <td>200</td>
      </tr>
      <tr>
        <td>7</td>
        <td>250</td>
      </tr>
      <tr>
        <td>8</td>
        <td>320</td>
      </tr>
      <tr>
        <td>9</td>
        <td>400</td>
      </tr>
      <tr>
        <td>10</td>
        <td>500</td>
      </tr>
      <tr>
        <td>11</td>
        <td>640</td>
      </tr>
      <tr>
        <td>12</td>
        <td>800</td>
      </tr>
      <tr>
        <td>13</td>
        <td>1000</td>
      </tr>
      <tr>
        <td>14</td>
        <td>1250</td>
      </tr>
      <tr>
        <td>15</td>
        <td>1600</td>
      </tr>
      <tr>
        <td>16</td>
        <td>2000</td>
      </tr>
      <tr>
        <td>17</td>
        <td>2500</td>
      </tr>
      <tr>
        <td>18</td>
        <td>3200</td>
      </tr>
      <tr>
        <td>19</td>
        <td>4000 (RICOH THETA X is not supported)</td>
      </tr>
      <tr>
        <td>20</td>
        <td>5000 (RICOH THETA X is not supported)</td>
      </tr>
      <tr>
        <td>21</td>
        <td>6400 (RICOH THETA X is not supported)</td>
      </tr>
    </tbody>
  </table> 

## ISO Sensitivity Upper Limit

Set the ISO sensitivity upper limit with "RIC_AEC_MAXISO_STILL" for images and "RIC_AEC_MAXISO_VIDEO" for videos.
To set ISO sensitivity upper limit, set the value (int type) for "RIC_AEC_MAXISO_STILL" and "RIC_AEC_MAXISO_VIDEO".

When the model of the camera is RICOH THETA V, in image shooting mode, a value of 200 to 3200 can be set.
When the camera model is RICOH THETA V, and it is in movie shooting mode, a value of 200 to 6400 can be set. 
When the model of the camera is RICOH THETA Z1, in image shooting mode or video recording mode, a value of 200 to 6400 can be set.
When the model of the camera is RICOH THETA X, in image shooting mode or video recording mode, a value of 100 to 3200 can be set.

<table>
    <thead>
      <tr>
        <th width="20%">Value</th>
        <th width="80%">Description</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>3</td>
        <td>100 (RICOH THETA X only)</td>
      </tr>
      <tr>
        <td>4</td>
        <td>125 (RICOH THETA X only)</td>
      </tr>
      <tr>
        <td>5</td>
        <td>160 (RICOH THETA X only)</td>
      </tr>
      <tr>
        <td>6</td>
        <td>200</td>
      </tr>
      <tr>
        <td>7</td>
        <td>250</td>
      </tr>
      <tr>
        <td>8</td>
        <td>320</td>
      </tr>
      <tr>
        <td>9</td>
        <td>400</td>
      </tr>
      <tr>
        <td>10</td>
        <td>500</td>
      </tr>
      <tr>
        <td>11</td>
        <td>640</td>
      </tr>
      <tr>
        <td>12</td>
        <td>800</td>
      </tr>
      <tr>
        <td>13</td>
        <td>1000</td>
      </tr>
      <tr>
        <td>14</td>
        <td>1250</td>
      </tr>
      <tr>
        <td>15</td>
        <td>1600</td>
      </tr>
      <tr>
        <td>16</td>
        <td>2000</td>
      </tr>
      <tr>
        <td>17</td>
        <td>2500</td>
      </tr>
      <tr>
        <td>18</td>
        <td>3200</td>
      </tr>
      <tr>
        <td>19</td>
        <td>4000 (RICOH THETA X is not supported)</td>
      </tr>
      <tr>
        <td>20</td>
        <td>5000 (RICOH THETA X is not supported)</td>
      </tr>
      <tr>
        <td>21</td>
        <td>6400 (RICOH THETA X is not supported)</td>
      </tr>
    </tbody>
  </table> 

## Aperture

To set aperture, set the value (int type) for "RIC_MANUAL_EXPOSURE_AV_FRONT" and "RIC_MANUAL_EXPOSURE_AV_REAR". This parameter is valid only when "RIC_EXPOSURE_MODE" is set to "RicAutoExposureA" or "RicManualExposure". It is recommended that the same value be set for "RIC_MANUAL_EXPOSURE_AV_FRONT" and "RIC_MANUAL_EXPOSURE_AV_REAR". There is no guarantee of the action if different values are set.  
This KEY is available only with RICOH THETA Z1.

<table>
    <thead>
      <tr>
        <th width="20%">Value</th>
        <th width="80%">Description</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>0</td>
        <td>F2.1</td>
      </tr>
      <tr>
        <td>1</td>
        <td>F3.5</td>
      </tr>
      <tr>
        <td>2</td>
        <td>F5.6</td>
      </tr>
    </tbody>
  </table> 

## White Balance
To set white balance, set the value (String type) for "RIC_WB_MODE".

|Value|Description|
|:-|:-|
|"RicWbAuto"|Same as WHITE_BALANCE_AUTO|
|"RicWbPreviousGain"|Use same gain as previous WB (not update WB)|
|"RicWbPrefixTemperature"|Use color temperature|
|"RicWbPrefixDaylight"|Same as WHITE_BALANCE_DAYLIGHT|
|"RicWbPrefixShade"|Same as WHITE_BALANCE_SHADE|
|"RicWbPrefixCloudyDaylight"|Same as WHITE_BALANCE_CLOUDY_DAYLIGHT|
|"RicWbPrefixIncandescent"|Same as WHITE_BALANCE_INCANDESCENT|
|"RicWbPrefixFluorescentWW"|Same as WHITE_BALANCE_WARM_FLUORESCENT|
|"RicWbPrefixFluorescentD"|Daylight Fluorescent|
|"RicWbPrefixFluorescentN"|Daywhite Fluorescent|
|"RicWbPrefixFluorescentW"|Same as WHITE_BALANCE_FLUORESCENT|
|"RicWbPrefixFluorescentL"|Bulb Fluorescent|
|"RicWbAutoUnderwater"|Underwater (RICOH THETA Z1 is not supported)|

## Color Temperature
When "RicWbManualGain" is set in white balance, then set the value (int type) for "RIC_WB_TEMPERATURE" in the Color Temperature setting. 

|Value|Description|
|:-|:-|
|2500 - 10000|Range: Between 2500-10000K|

## White Balance Auto Strength
To set the strength of white balance auto for low color temperature scene, set the value (int type) to "RIC_WB_STRENGTH".  
This KEY is available with RICOH THETA Z1 firmware v2.20.3 or later.

|Value|Description|
|:-|:-|
|0|not correct tint for low color temperature scene (default)|
|1|    correct tint for low color temperature scene |

## Exposure Compensation
To set exposure compensation, set the value (int type) for "exposure-compensation-step". When "RIC_EXPOSURE_MODE" is "RicManualExposure", it can only be set to 0.0. When "RIC_EXPOSURE_MODE" is "RicAutoExposureP", "RicAutoExposureA", "RicAutoExposureT", "RicAutoExposureS", or "RicAutoExposureWDR", from -2.0 to 2.0 can be set. 

|Value|Description|
|:-|:-|
|-6|-2.0 Ev|
|-5|-1.7 Ev|
|-4|-1.3 Ev|
|-3|-1.0 Ev|
|-2|-0.7 Ev|
|-1|-0.3 Ev|
|0|0.0 Ev|
|1|0.3 Ev|
|2|0.7 Ev|
|3|1.0 Ev|
|4|1.3 Ev|
|5|1.7 Ev|
|6|2.0 Ev|

## Activate Image File Size Specification

Set "RIC_JPEG_COMP_FILESIZE_ENABLED" to enable or disable the image file size specified by "RIC_JPEG_COMP_FILESIZE".
To set activate image file size specification, set the value (int type) for "RIC_JPEG_COMP_FILESIZE_ENABLED".

|Value|Description|
|:-|:-|
|0|disable|
|1|enable|

## Image File Size

Set the image file size with "RIC_JPEG_COMP_FILESIZE".
To set image file size, set the value (int type) for "RIC_JPEG_COMP_FILESIZE".

### RICOH THETA V, Z1
From 1048576 (1MByte) to 12582912 (12MByte)

V: 4 MByte, Z1: 8 MByte.

### RICOH THETA X
From 1048576 (1MByte) to 20971520 (20MByte)

10 MByte for 11K, 4 MByte for 5.5K.

## Switching DNG Output

Set activation / deactivation of DNG file output with "RIC_DNG_OUTPUT_ENABLED".
To set switching DNG output, set the value (int type) for "RIC_DNG_OUTPUT_ENABLED".

|Value|Description|
|:-|:-|
|0|disable|
|1|enable|

## Burst Capture Mode

Burst Capture Mode is to shoot JPEG or DNG images as the highest FPS capturing, upto 9 frames as maximum.
Remark
* Set RIC_SHOOTING_MODE to "RicStillCaptureStdBurst" before "startPreview".
* "PictureCallBack" will be sent to application layer same times as the number of captured frames.
* When using RIC_DNG_OUTPUT_ENABLED=1, this mode will output DNG images only. JPEG images cannot be output.
* DNG images will be stored in DCIM/0/temp[0-8].dng.
* This feature can be used with RICOH THETA Z1 firmware v2.00 or later
* RICOH THETA X/V/SC/S is not supported.

#### RIC_AEC_BURST_CAPTURE_NUM

To set the number of burst capture frames, set value (int type) for "RIC_AEC_BURST_CAPTURE_NUM". Default value is 1.

|Value|Description|
|:-|:-|
|1|1 frame|
|3|3 frames|
|5|5 frames|
|7|7 frames|
|9|9 frames|

#### RIC_AEC_BURST_BRACKET_STEP

To set the bracket step of burst capture mode, set value (int type) for "RIC_AEC_BURST_BRACKET_STEP". Default value is 0.

|Value|Description|
|:-|:-|
|0|0.0 Ev, this means to capture all frames with same exposure setting.|
|1|0.3 Ev|
|2|0.7 Ev|
|3|1.0 Ev|
|4|1.3 Ev|
|5|1.7 Ev|
|6|2.0 Ev|
|7|2.3 Ev|
|8|2.7 Ev|
|9|3.0 Ev|

#### RIC_AEC_BURST_COMPENSATION

To set the exposure compensation of burst capture mode, set value (int type) for "RIC_AEC_BURST_COMPENSATION". Default value is 0.

|Value|Description|
|:-|:-|
|-15|-5.0 Ev|
|-14|-4.7 Ev|
|-13|-4.3 Ev|
|-12|-4.0 Ev|
|-11|-3.7 Ev|
|-10|-3.3 Ev|
|-9|-3.0 Ev|
|-8|-2.7 Ev|
|-7|-2.3 Ev|
|-6|-2.0 Ev|
|-5|-1.7 Ev|
|-4|-1.3 Ev|
|-3|-1.0 Ev|
|-2|-0.7 Ev|
|-1|-0.3 Ev|
|0|0.0 Ev|
|1|+0.3 Ev|
|2|+0.7 Ev|
|3|+1.0 Ev|
|4|+1.3 Ev|
|5|+1.7 Ev|
|6|+2.0 Ev|
|7|+2.3 Ev|
|8|+2.7 Ev|
|9|+3.0 Ev|
|10|+3.3 Ev|
|11|+3.7 Ev|
|12|+4.0 Ev|
|13|+4.3 Ev|
|14|+4.7 Ev|
|15|+5.0 Ev|

#### RIC_AEC_BURST_MAX_EXPOSURE_TIME

To set the upper limit of exposure time of burst capture mode, set value (int type) for "RIC_AEC_BURST_MAX_EXPOSURE_TIME". Default value is 56.

|Value|Description|
|:-|:-|
|0|1/25000 sec|
|1|1/20000 sec|
|2|1/16000 sec|
|3|1/12500 sec|
|4|1/10000 sec|
|5|1/8000 sec|
|6|1/6400 sec|
|7|1/5000 sec|
|8|1/4000 sec|
|9|1/3200 sec|
|10|1/2500 sec|
|11|1/2000 sec|
|12|1/1600 sec|
|13|1/1250 sec|
|14|1/1000 sec|
|15|1/800 sec|
|16|1/640 sec|
|17|1/500 sec|
|18|1/400 sec|
|19|1/320 sec|
|20|1/250 sec|
|21|1/200 sec|
|22|1/160 sec|
|23|1/125 sec|
|24|1/100 sec|
|25|1/80 sec|
|26|1/60 sec|
|27|1/50 sec|
|28|1/40 sec|
|29|1/30 sec|
|30|1/25 sec|
|31|1/20 sec|
|32|1/15 sec|
|33|1/13 sec|
|34|1/10 sec|
|35|1/8 sec|
|36|1/6 sec|
|37|1/5 sec|
|38|1/4 sec|
|39|1/3 sec|
|40|1/2.5 sec|
|41|1/2 sec|
|42|1/1.6 sec|
|43|1/1.3 sec|
|44|1.0 sec|
|45|1.3 sec|
|46|1.6 sec|
|47|2 sec|
|48|2.5 sec|
|49|3.2 sec|
|50|4 sec|
|51|5 sec|
|52|6 sec|
|53|8 sec|
|54|10 sec|
|55|13 sec|
|56|15 sec|
|57|20 sec|
|58|25 sec|
|59|30 sec|
|60|40 sec|
|61|50 sec|
|62|60 sec|

#### RIC_AEC_BURST_ENABLE_ISO_CONTROL

To set the auto ISO control of burst capture mode, set value (int type) for “RIC_AEC_BURST_ENABLE_ISO_CONTROL”.  
To set "RIC_AEC_BURST_ENABLE_ISO_CONTROL" to 1, ISO sensitivity will be set higher value when exposure time reach to RIC_AEC_BURST_MAX_EXPOSURE_TIME. Default value is 0.

|Value|Description|
|:-|:-|
|0|Disable to auto ISO control. This means to set always ISO80 when auto exposure mode.|
|1|Enable to auto ISO control. This means to allow higher ISO sensitivity.|

#### RIC_AEC_BURST_ORDER

To set the shooting order of exposure setting, set value (int type) for “RIC_AEC_BURST_ORDER”. This API is available with THETA Z1 firmware v2.10.3 or later. 

|Value|Description|
|:-|:-|
|0| `0` > `-` > `+` (default)|
|1| `-` > `0` > `+`|

## Face Detection
To enable Face Detection feature, set the value (int type) for “RIC_FACE_DETECTION”. AE will make detected human faces brighter when this feature is enabled. Only available in still capture mode of RICOH THETA X. Default value is 0.

|Value|Description|
|:-|:-|
|0|OFF|
|1|ON|
