# Camera API

**RICOH THETA V and Z1** support `android.hardware.Camera package` to control the 360° camera. To use camera resources, the plugin app must send a specified Broadcast Intent [Notify Camera Resource Control Change](./broadcast-intent.md#notify-camera-resource-control-change).  

> [!NOTE]  
> RICOH THETA V and Z1 do not support the `android.hardware.camera2 package`.

**RICOH THETA X** supports `com.theta360.hardware.Camera` package to control the 360° camera. Plugin apps must import these packages via [THETA Plugin Library](https://github.com/ricohapi/theta-plugin-library).

Below are sample projects demonstrating how to control camera functions via the Camera API in a RICOH THETA plugin:

* [THETA Plugin: CameraAPI Sample](https://github.com/ricohapi/theta-plugin-camera-api-sample) - for THETA V, Z1, and X.
* [THETA X Plugin : Camera API Sample](https://github.com/ricohapi/theta-plugin-camera-api-sample-x) - for THETA X.

----

RICOH THETA V, Z1, and X define custom parameters, as listed below. These can be set using `Camera.Parameters.set()` API.  

### Contents

* [Shooting Mode](#shooting-mode)
* [Stitching](#stitching)
* [Zenith Correction](#zenith-correction)
* [Exposure Program](#exposure-program)
* [Lock Auto Exposure](#lock-auto-exposure)
* [Exposure Time](#exposure-time)
* [ISO Sensitivity](#iso-sensitivity)
* [ISO Sensitivity Upper Limit](#iso-sensitivity-upper-limit)
* [Aperture](#aperture)
* [HDR Bracket Setting](#hdr-bracket-setting)
* [White Balance](#white-balance)
* [Exposure Compensation](#exposure-compensation)
* [Custome Image File Size](#custom-image-file-size)
* [DNG Output](#dng-output)
* [Burst Capture Mode](#burst-capture-mode)
* [Face Detection](#face-detection)

## Shooting Mode

#### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) |
|:-:|:-:|:-:|
| ✓ | ✓ | ✓ | 

| | |
|:--|:--|
| **Key**  | `RIC_SHOOTING_MODE` |
| **Type** | String |

#### RICOH THETA V, Z1

| Value | Mode | Description |
|:--|:--|:--|
| `RicMonitoring"`<sup>\*1</sup> | Preview | Use special preview mode to reduce the shutter time lag when capturing still images. This mode is not compatible with NR, HDR, or HhHDR modes, and cannot be used with Web API `camera.getLivePreview`. |
| `RicMoviePreview640`  | Preview | 640x320px preview |
| `RicMoviePreview1024` | Preview | 1024x512px preview |
| `RicMoviePreview1920` | Preview | 1920x960px preview |
| `RicMoviePreview3840` | Preview | 3840x1920px preview |
| `RicStillCaptureStd`  | Still Image | Normal mode |
| `RicStillCaptureStdBurst`<sup>\*2</sup> | Still Image | Burst capture mode |
| `RicStillCaptureWDR` | Still Image | DR correction mode |
| `RicStillCaptureMultiRawNR`  | Still Image | Noise Reduction mode |
| `RicStillCaptureMultiYuvHdr` | Still Image | HDR Rendering mode |
| `RicStillCaptureMultiYuvHhHdr`<sup>\*3</sup> | Still Image | Handheld HDR mode |
| `RicMovieRecording4kEqui`<sup>\*4</sup> | Video Recording | 3840x1920px video with Equirectangular format |
| `RicMovieRecording4kDual`<sup>\*4</sup> | Video Recording | 3840x1920px video with Dual Fisheye format |
| `RicMovieRecording2kEqui`<sup>\*4</sup> | Video Recording | 1920x960px video with Equirectangular format |
| `RicMovieRecording2kDual`<sup>\*4</sup> | Video Recording | 1920x960px video with Dual Fisheye format |

<sup>\*1</sup>Only available on THETA Z1  
<sup>\*2</sup>THETA Z1 firmware v2.00.1 and later. Please refer to [Burst Capture Mode](#burst-capture-mode) for detail.  
<sup>\*3</sup>THETA Z1 firmware v1.20.1 and later, and THETA V firmware v3.10.1 and later  
<sup>\*4</sup>To apply this change, the [Stitching](#stitching) setting `RIC_PROC_STITCHING` is also required.  

#### RICOH THETA X

| Value | Mode | Description |
|:--|:--|:--|
| `RicPreviewFront` | Preview | 512x512px preview, available only with `CAMERA_FACING_FRONT`|
| `RicPreviewRear`  | Preview | 512x512px preview, available only with `CAMERA_FACING_BACK` |
| `RicPreview1024` | Preview | 1024x512px preview |
| `RicPreview1920` | Preview | 1920x960px preview |
| `RicPreview3840` | Preview | 3840x1920px preview |
| `RicPreview5760` | Preview | 5760x2880px preview |
| `RicPreview1024:576`  | Preview | 1024x576px (16:9 aspect ratio) preview |
| `RicPreview1920:1080` | Preview | 1920x1080px (16:9 aspect ratio) preview |
| `RicPreview3840:2160` | Preview | 3840x2160px (16:9 aspect ratio) preview |
| `RicStillCaptureStd`  | Still Image | Normal mode |
| `RicStillCaptureMultiRawNR`  | Still Image | Noise Reduction mode |
| `RicStillCaptureMultiYuvHdr` | Still Image | HDR Rendering mode |
| `RicStillCaptureMultiYuvHhHdr`<sup>\*1</sup> | Still Image | Handheld HDR mode |
| `RicMovieRecording1920` | Video Recording | 1920x960px video |
| `RicMovieRecording3840` | Video Recording | 3840x1920px video |
| `RicMovieRecording5760` | Video Recording | 5760x2880px video |
| `RicMovieRecording7680`<sup>\*2</sup> | Video Recording | 7680x3840px video |

<sup>\*1</sup>THETA X firmware v2.40.0 and later  
<sup>\*2</sup>8K video mode is available at up to 10 fps. The plugin app must set the frame rate using a method such as `setVideoFrameRate(10)`. 8K video can be encoded using an I-frame-only configuration. The plugin app must set the I-frame interval using a method such as `setVideoEncodingIFrameInterval(0.0f)`.  

## Stitching

#### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) |
|:-:|:-:|:-:|
| ✓ | ✓ | ✓ | 

| | |
|:--|:--|
| **Key**  | `RIC_PROC_STITCHING` |
| **Type** | String |

| Value | Description |
|:--|:--|
| `RicNonStitching` | As no stitching is applied, the image is output in Dual Fisheye format. |
| `RicStaticStitching` | Stitching is applied, with dewarping based on a static transformation table. |
| `RicDynamicStitchingAuto`<sup>\*1</sup> | Stitching is applied, using a dynamic algorithm that adapts to the subject. |

> [!IMPORTANT]  
> <sup>\*1</sup>RICOH V and Z1 can use `RicDynamicStitchingAuto` only for still image mode.  

### Stitching Mode with Water Housing TW-2

To optimize stitching process with using water housing TW-2.  

#### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) |
|:-:|:-:|:-:|
| ✓<sup>\*1</sup> ||| 

<sup>\*1</sup>THETA X firmware v1.40.0 and later  

| | |
|:--|:--|
| **Key**  | `RIC_WATER_HOUSING` |
| **Type** | Int |

| Value | Description |
|:--:|:--|
| `0` | Not use TW-2 (Deault)  |
| `1` | Use TW-2 in underwater |
| `2` | Use TW-2 on land |

## Zenith Correction

#### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) |
|:-:|:-:|:-:|
| ✓ | ✓ | ✓ |

| | |
|:--|:--|
| **Key**  | `RIC_PROC_ZENITH_CORRECTION` |
| **Type** | String |

| Value | Description |
|:--|:--|
| `RicZenithCorrectionOff` | No Zenith correction is applied  |
| `RicZenithCorrectionOnAuto` | Zenith correction is automatically applied based on orientation data obtained from the IMU |
| `RicZenithCorrectionOnManual`<sup>\*1</sup> | Zenith correction is applied using a fixed rotation angle |

<sup>\*1</sup>Available only on the THETA X. A fixed rotation angle can be set using the `RIC_ZENITH_DIRECTION` parameter. The value must be a String in the format `"%.02f_%.02f_%.02f"`.
For example, `"15.00_30.00_45.00"` represents a pitch of 15.00°, roll of 30.00°, and yaw of 45.00°.  

> [!IMPORTANT]  
> On the THETA V and Z1, a specified Broadcast Intent must be sent to [Control IMU](./broadcast-intent.md#control-imu) in order to start the IMU and enable zenith correction before capturing with the Camera API.  

## Exposure Program

#### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) |
|:-:|:-:|:-:|
| ✓ | ✓ | ✓ |

| | |
|:--|:--|
| **Key**  | `RIC_EXPOSURE_MODE` |
| **Type** | String |

| Value | Description |
|:--|:--|
| `RicAutoExposureP`  | Program auto exposure mode |
| `RicAutoExposureA`<sup>\*1</sup> | Av priority mode (Av=aperture) |
| `RicAutoExposureT`  | Tv priority mode (Tv=exposure time)   |
| `RicAutoExposureS`  | Sv priority mode (Sv=ISO sensitivity) |
| `RicManualExposure` | Manual exposure mode |

<sup>\*1</sup>Available only on the THETA Z1

### Lock Auto Exposure

#### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) |
|:-:|:-:|:-:|
|   | ✓ | ✓ |

| | |
|:--|:--|
| **Key**  | `“RIC_EXPOSURE_LOCK”` |
| **Type** | Int |

| Value | Description |
|:--:|:--|
| `0` | Unlock auto exposure controll (default) |
| `1` | Lock auto exposure controll |

## Exposure Time

#### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) |
|:-:|:-:|:-:|
| ✓ | ✓ | ✓ |

| | |
|:--|:--|
| **Key**  | `RIC_MANUAL_EXPOSURE_TIME_FRONT`<br>`RIC_MANUAL_EXPOSURE_TIME_REAR` |
| **Type** | Int |

This parameter is valid only when `RIC_EXPOSURE_MODE` is set to either `RicManualExposure` or `RicAutoExposureT`. When using `RicAutoExposureT`, only values between 1/25000 sec and 15 sec can be set.<sup>\*1</sup>  

> [!IMPORTANT]  
> It is recommended to set the same value for `RIC_MANUAL_EXPOSURE_TIME_FRONT and RIC_MANUAL_EXPOSURE_TIME_REAR`. The behavior is not guaranteed if different values are used.  

<sup>\*1</sup>For THETA Z1 firmware v1.50.1 and earlier and THETA V firmware v3.40.1 and earlier, exposure time from 1/25000 sec to **1/8 sec** can be set.  

| Value | Description |
|:--:|:--|
| `-1` | Auto |
| `0`<sup>\*2</sup> | 1/25000 sec |
| `1`<sup>\*2</sup> | 1/20000 sec |
| `2` | 1/16000 sec |
| `3` | 1/12500 sec - THETA V, Z1<br>1/12800 sec - THETA X |
| `4` | 1/10000 sec |
| `5` | 1/8000 sec |
| `6` | 1/6400 sec |
| `7` | 1/5000 sec |
| `8` | 1/4000 sec |
| `9` | 1/3200 sec |
| `10` | 1/2500 sec |
| `11` | 1/2000 sec |
| `12` | 1/1600 sec |
| `13` | 1/1250 sec |
| `14` | 1/1000 sec |
| `15` | 1/800 sec |
| `16` | 1/640 sec |
| `17` | 1/500 sec |
| `18` | 1/400 sec |
| `19` | 1/320 sec |
| `20` | 1/250 sec |
| `21` | 1/200 sec |
| `22` | 1/160 sec |
| `23` | 1/125 sec |
| `24` | 1/100 sec |
| `25` | 1/80 sec |
| `26` | 1/60 sec |
| `27` | 1/50 sec |
| `28` | 1/40 sec |
| `29` | 1/30 sec |
| `30` | 1/25 sec |
| `31` | 1/20 sec |
| `32` | 1/15 sec |
| `33` | 1/13 sec |
| `34` | 1/10 sec |
| `35` | 1/8 sec |
| `36` | 1/6 sec |
| `37` | 1/5 sec |
| `38` | 1/4 sec |
| `39` | 1/3 sec |
| `40` | 1/2.5 sec |
| `41` | 1/2 sec |
| `42` | 1/1.6 sec |
| `43` | 1/1.3 sec |
| `44` | 1/1 sec |
| `45` | 1.3 sec |
| `46` | 1.6 sec |
| `47` | 2 sec |
| `48` | 2.5 sec |
| `49` | 3.2 sec |
| `50` | 4 sec |
| `51` | 5 sec |
| `52` | 6 sec |
| `53` | 8 sec |
| `54` | 10 sec |
| `55` | 13 sec |
| `56` | 15 sec |
| `57` | 20 sec |
| `58` | 25 sec |
| `59` | 30 sec |
| `60`<sup>\*3</sup> | 40 sec |
| `61`<sup>\*3</sup> | 50 sec |
| `62` | 60 sec |

<sup>\*2</sup>THETA X does not support  
<sup>\*3</sup>THETA V and Z1 do not support  

## ISO Sensitivity

#### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) |
|:-:|:-:|:-:|
| ✓ | ✓ | ✓ |

| | |
|:--|:--|
| **Key**  | `RIC_MANUAL_EXPOSURE_ISO_FRONT`<br>`RIC_MANUAL_EXPOSURE_ISO_REAR` |
| **Type** | Int |

| Model | Mode | Supported Value Range |
|:--|:--|:--|
| THETA V  | Still Image     | ISO 64 - 3200 |
|          | Video Recording | ISO 64 - 6400 |
| THETA Z1 | Still Image     | ISO 80 - 6400 |
|          | Video Recording | ISO 64 - 6400 |
| THETA X  | Still Image     | ISO 50 - 3200 |
|          | Video Recording | ISO 50 - 3200 |

This parameter is valid only when `RIC_EXPOSURE_MODE` is set to either `RicManualExposure` or `RicAutoExposureS`.  

> [!IMPORTANT]  
> It is recommended to set the same value for `RIC_MANUAL_EXPOSURE_ISO_FRONT` and `RIC_MANUAL_EXPOSURE_ISO_REAR`. The behavior is not guaranteed if different values are used.  

| Value | Description |
|:--:|:--|
| `-1` | Auto |
| `0`  | ISO 50 |
| `1`  | ISO 64 |
| `2`  | ISO 80 |
| `3`  | ISO 100 |
| `4`  | ISO 125 |
| `5`  | ISO 160 |
| `6`  | ISO 200 |
| `7`  | ISO 250 |
| `8`  | ISO 320 |
| `9`  | ISO 400 |
| `10` | ISO 500 |
| `11` | ISO 640 |
| `12` | ISO 800 |
| `13` | ISO 1000 |
| `14` | ISO 1250 |
| `15` | ISO 1600 |
| `16` | ISO 2000 |
| `17` | ISO 2500 |
| `18` | ISO 3200 |
| `19` | ISO 4000 |
| `20` | ISO 5000 |
| `21` | ISO 6400 |

### ISO Sensitivity Upper Limit

#### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) |
|:-:|:-:|:-:|
| ✓ | ✓ | ✓ |

| | |
|:--|:--|
| **Key**  | `RIC_AEC_MAXISO_STILL`<br>`RIC_AEC_MAXISO_VIDEO` |
| **Type** | Int |

| Model | Mode | Supported Value Range |
|:--|:--|:--|
| THETA V  | Still Image     | ISO 200 - 3200 |
|          | Video Recording | ISO 200 - 6400 |
| THETA Z1 | Still Image     | ISO 200 - 6400 |
|          | Video Recording | ISO 200 - 6400 |
| THETA X  | Still Image     | ISO 100 - 3200 |
|          | Video Recording | ISO 100 - 3200 |

| Value | Description |
|:--:|:--|
| `3`  | ISO 100 |
| `4`  | ISO 125 |
| `5`  | ISO 160 |
| `6`  | ISO 200 |
| `7`  | ISO 250 |
| `8`  | ISO 320 |
| `9`  | ISO 400 |
| `10` | ISO 500 |
| `11` | ISO 640 |
| `12` | ISO 800 |
| `13` | ISO 1000 |
| `14` | ISO 1250 |
| `15` | ISO 1600 |
| `16` | ISO 2000 |
| `17` | ISO 2500 |
| `18` | ISO 3200 |
| `19` | ISO 4000 |
| `20` | ISO 5000 |
| `21` | ISO 6400 |

## Aperture

#### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) |
|:-:|:-:|:-:|
|   | ✓ |   |

| | |
|:--|:--|
| **Key**  | `RIC_MANUAL_EXPOSURE_AV_FRONT`<br>`RIC_MANUAL_EXPOSURE_AV_REAR` |
| **Type** | Int |

This parameter is valid only when `RIC_EXPOSURE_MODE` is set to either `RicManualExposure` or `RicAutoExposureA`.  

> [!IMPORTANT]  
> It is recommended to set the same value for `RIC_MANUAL_EXPOSURE_AV_FRONT` and `RIC_MANUAL_EXPOSURE_AV_REAR`. The behavior is not guaranteed if different values are used.  

| Value | Description |
|:--:|:--|
| `0` | F2.1 |
| `1` | F3.5 |
| `2` | F5.6 |

## HDR Bracket Setting

#### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) |
|:-:|:-:|:-:|
| ✓<sup>\*1</sup> |||

<sup>\*1</sup>THETA X firmware v2.50.2 and later  

| | |
|:--|:--|
| **Key**  | `RIC_HDR_BRACKET` |
| **Type** | Int |

| Value | Description |
|:--:|:--|
| `0` | -4Ev / ±0Ev / +2Ev (default) |
| `1` | -1Ev / ±0Ev / +1Ev |
| `2` | -2Ev / ±0Ev / +1Ev |
| `3` | -3Ev / ±0Ev / +3Ev |
| `4` | -4Ev / ±0Ev / +4Ev |
| `5` | -5Ev / ±0Ev / +2Ev |

## White Balance

#### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) |
|:-:|:-:|:-:|
| ✓ | ✓ | ✓ |

| | |
|:--|:--|
| **Key**  | `RIC_WB_MODE` |
| **Type** | String |

| Value | Description |
|:--|:--|
| `RicWbAuto` | Auto. Same as `WHITE_BALANCE_AUTO` defined in Android OS |
| `RicWbPreviousGain`<sup>\*1</sup> | Use same gain as previous capture (not update WB) |
| `RicWbPrefixTemperature` | Use fixed color temperature. Refer to [White Balance Color Temperature](#white-balance-color-temperature). |
| `RicWbPrefixDaylight`    | Same as `WHITE_BALANCE_DAYLIGHT` defined in Android OS |
| `RicWbPrefixShade`       | Same as `WHITE_BALANCE_SHADE` defined in Android OS |
| `RicWbPrefixCloudyDaylight` | Same as `WHITE_BALANCE_CLOUDY_DAYLIGHT` defined in Android OS |
| `RicWbPrefixIncandescent`  | Same as `WHITE_BALANCE_INCANDESCENT` defined in Android OS |
| `RicWbPrefixFluorescentWW` | Same as `WHITE_BALANCE_WARM_FLUORESCENT` defined in Android OS |
| `RicWbPrefixFluorescentD` | Daylight Fluorescent |
| `RicWbPrefixFluorescentN` | Daywhite Fluorescent |
| `RicWbPrefixFluorescentW` | White Fluorescent, Same as `WHITE_BALANCE_FLUORESCENT` defined in Android OS |
| `RicWbPrefixFluorescentL`<sup>\*2</sup> | Bulb Fluorescent |

<sup>\*1</sup> THETA X does not support  
<sup>\*2</sup> THETA Z1 does not support  

### White Balance Color Temperature

#### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) |
|:-:|:-:|:-:|
| ✓ | ✓ | ✓ |

| | |
|:--|:--|
| **Key**  | `RIC_WB_TEMPERATURE` |
| **Type** | Int |

This parameter is valid only when `RIC_WB_MODE` is set to `RicWbPrefixTemperature`.  

| Value | Description |
|:--|:--|
| `2500` - `10000` | Can be specified in 100-Kelvin increments |

### White Balance Auto Strength

#### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) |
|:-:|:-:|:-:|
|   | ✓<sup>\*3</sup> ||

<sup>\*3</sup>THETA Z1 firmware v2.20.3 and later  

| | |
|:--|:--|
| **Key**  | `RIC_WB_STRENGTH` |
| **Type** | Int |

| Value | Description |
|:--:|:--|
| `0` | Not correct tint for low color temperature scene (default) |
| `1` |     Correct tint for low color temperature scene |

## Exposure Compensation

#### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) |
|:-:|:-:|:-:|
| ✓ | ✓ | ✓ |

| | |
|:--|:--|
| **Key**  | `exposure-compensation-step` |
| **Type** | Int |

This parameter is valid only when `RIC_EXPOSURE_MODE` is set to either `RicAutoExposureP`, `RicAutoExposureA`, `RicAutoExposureT`, `RicAutoExposureS`, or `RicAutoExposureWDR`.  

| Value | Description|
|:--:|:--|
| `-6` | -2.0 Ev |
| `-5` | -1.7 Ev |
| `-4` | -1.3 Ev |
| `-3` | -1.0 Ev |
| `-2` | -0.7 Ev |
| `-1` | -0.3 Ev |
| `0`  |  0.0 Ev |
| `1`  |  0.3 Ev |
| `2`  |  0.7 Ev |
| `3`  |  1.0 Ev |
| `4`  |  1.3 Ev |
| `5`  |  1.7 Ev |
| `6`  |  2.0 Ev |

## Custom Image File Size

#### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) |
|:-:|:-:|:-:|
| ✓ | ✓ | ✓ |

| | |
|:--|:--|
| **Key**  | `RIC_JPEG_COMP_FILESIZE_ENABLED` |
| **Type** | Int |

| Value | Description |
|:--:|:--|
| `0` | Disable custom image file size |
| `1` | Enable custom image file size  |

When `RIC_JPEG_COMP_FILESIZE_ENABLE` is set to `1`, you can specify the target JPEG file size by setting a value for the `RIC_JPEG_COMP_FILESIZE` key.

| | |
|:--|:--|
| **Key**  | `RIC_JPEG_COMP_FILESIZE` |
| **Type** | Int |

| Model | Supported Value Range |
|:--|:--|
| THETA V  | `1048576` (1MB) to `12582912` (12MB), default value is 4MB. |
| THETA Z1 | `1048576` (1MB) to `12582912` (12MB), default value is 8MB. |
| THETA X  | `1048576` (1MB) to `20971520` (20MB), default value is 4MB@5,5K, 10MB@11K. |

## DNG Output

| | |
|:--|:--|
| **Key**  | `RIC_DNG_OUTPUT_ENABLED` |
| **Type** | Int |

#### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) |
|:-:|:-:|:-:|
|   | ✓ |   |

|Value|Description|
|:--:|:--|
| `0` | Disable dng output |
| `1` | Enable dng output  |

> [!NOTE]  
> The DNG file is stored at `DCIM/temp.dng` when a photo is taken.  

## Burst Capture Mode

Burst Capture Mode captures JPEG or DNG images at the highest possible frame rate, up to a maximum of 9 frames.

> [!NOTE]  
> * Set `RIC_SHOOTING_MODE` to `RicStillCaptureStdBurst` before calling `startPreview()`.
> * PictureCallback will be triggered as many times as the number of frames captured.
> * If `RIC_DNG_OUTPUT_ENABLED` is set to `1`, only DNG images will be output; JPEG images will not be generated.
> * DNG images are saved to `DCIM/0/temp[0-8].dng`.

#### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) |
|:-:|:-:|:-:|
|   | ✓<sup>\*1</sup> ||

<sup>\*1</sup>THETA Z1 firmware v2.00.1 and later  

#### RIC_AEC_BURST_CAPTURE_NUM

To set the number of burst capture frames.  

| | |
|:--|:--|
| **Key**  | `RIC_AEC_BURST_CAPTURE_NUM` |
| **Type** | Int |

| Value | Description |
|:--:|:--|
| `1` | 1 frame (default) |
| `3` | 3 frames |
| `5` | 5 frames |
| `7` | 7 frames |
| `9` | 9 frames |

#### RIC_AEC_BURST_BRACKET_STEP

To set the bracket step of burst capture mode.  

| | |
|:--|:--|
| **Key**  | `RIC_AEC_BURST_BRACKET_STEP` |
| **Type** | Int |

| Value | Description |
|:--:|:--|
| `0` | 0.0 Ev (default)<br>This means to capture all frames with same exposure setting |
| `1` | 0.3 Ev |
| `2` | 0.7 Ev |
| `3` | 1.0 Ev |
| `4` | 1.3 Ev |
| `5` | 1.7 Ev |
| `6` | 2.0 Ev |
| `7` | 2.3 Ev |
| `8` | 2.7 Ev |
| `9` | 3.0 Ev |

#### RIC_AEC_BURST_COMPENSATION

To set the exposure compensation of burst capture mode.

| Value | Description |
|:--:|:--|
| `-15` | -5.0 Ev |
| `-14` | -4.7 Ev |
| `-13` | -4.3 Ev |
| `-12` | -4.0 Ev |
| `-11` | -3.7 Ev |
| `-10` | -3.3 Ev |
| `-9` | -3.0 Ev |
| `-8` | -2.7 Ev |
| `-7` | -2.3 Ev |
| `-6` | -2.0 Ev |
| `-5` | -1.7 Ev |
| `-4` | -1.3 Ev |
| `-3` | -1.0 Ev |
| `-2` | -0.7 Ev |
| `-1` | -0.3 Ev |
| `0` |  0.0 Ev |
| `1` | +0.3 Ev |
| `2` | +0.7 Ev |
| `3` | +1.0 Ev |
| `4` | +1.3 Ev |
| `5` | +1.7 Ev |
| `6` | +2.0 Ev |
| `7` | +2.3 Ev |
| `8` | +2.7 Ev |
| `9` | +3.0 Ev |
| `10` | +3.3 Ev |
| `11` | +3.7 Ev |
| `12` | +4.0 Ev |
| `13` | +4.3 Ev |
| `14` | +4.7 Ev |
| `15` | +5.0 Ev |

#### RIC_AEC_BURST_MAX_EXPOSURE_TIME

To set the maximum exposure time of burst capture mode.

| Value | Description |
|:--:|:--|
| `0` | 1/25000 sec |
| `1` | 1/20000 sec |
| `2` | 1/16000 sec |
| `3` | 1/12500 sec |
| `4` | 1/10000 sec |
| `5` | 1/8000 sec |
| `6` | 1/6400 sec |
| `7` | 1/5000 sec |
| `8` | 1/4000 sec |
| `9` | 1/3200 sec |
| `10` | 1/2500 sec |
| `11` | 1/2000 sec |
| `12` | 1/1600 sec |
| `13` | 1/1250 sec |
| `14` | 1/1000 sec |
| `15` | 1/800 sec |
| `16` | 1/640 sec |
| `17` | 1/500 sec |
| `18` | 1/400 sec |
| `19` | 1/320 sec |
| `20` | 1/250 sec |
| `21` | 1/200 sec |
| `22` | 1/160 sec |
| `23` | 1/125 sec |
| `24` | 1/100 sec |
| `25` | 1/80 sec |
| `26` | 1/60 sec |
| `27` | 1/50 sec |
| `28` | 1/40 sec |
| `29` | 1/30 sec |
| `30` | 1/25 sec |
| `31` | 1/20 sec |
| `32` | 1/15 sec | 
| `33` | 1/13 sec |
| `34` | 1/10 sec |
| `35` | 1/8 sec |
| `36` | 1/6 sec |
| `37` | 1/5 sec |
| `38` | 1/4 sec |
| `39` | 1/3 sec |
| `40` | 1/2.5 sec |
| `41` | 1/2 sec |
| `42` | 1/1.6 sec |
| `43` | 1/1.3 sec |
| `44` | 1.0 sec |
| `45` | 1.3 sec |
| `46` | 1.6 sec |
| `47` | 2 sec |
| `48` | 2.5 sec |
| `49` | 3.2 sec |
| `50` | 4 sec |
| `51` | 5 sec |
| `52` | 6 sec |
| `53` | 8 sec |
| `54` | 10 sec |
| `55` | 13 sec |
| `56` | 15 sec (default) |
| `57` | 20 sec |
| `58` | 25 sec |
| `59` | 30 sec |
| `60` | 40 sec |
| `61` | 50 sec |
| `62` | 60 sec |

#### RIC_AEC_BURST_ENABLE_ISO_CONTROL

To set the auto ISO control of burst capture mode.

| | |
|:--|:--|
| **Key**  | `RIC_AEC_BURST_ENABLE_ISO_CONTROL` |
| **Type** | Int |

|Value|Description|
|:--:|:--|
| `0` | Disable auto ISO control. This means to set always ISO80 when auto exposure mode. (default) |
| `1` | Enable auto ISO control. This means to allow higher ISO sensitivity. |

To set `RIC_AEC_BURST_ENABLE_ISO_CONTROL` to `1`, ISO sensitivity will be set higher value when exposure time reach to `RIC_AEC_BURST_MAX_EXPOSURE_TIME`.  

#### RIC_AEC_BURST_ORDER

To set the shooting order of exposure setting.  
This parameter is available with THETA Z1 firmware v2.10.3 and later.  

|Value|Description|
|:--:|:--|
| `0` | `0` > `-` > `+` (default) |
| `1` | `-` > `0` > `+` |

## Face Detection

#### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) |
|:-:|:-:|:-:|
| ✓ |||

| | |
|:--|:--|
| **Key**  | `RIC_FACE_DETECTION` |
| **Type** | Int |

To enable Face Detection feature. AE will make detected human faces brighter when this feature is enabled. Only available in still capture mode.

| Value | Description |
|:--:|:--|
| `0` | OFF (default) |
| `1` | ON |
