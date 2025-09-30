# Broadcast Intent

The plugin can send Broadcast Intent to control various hardware features, such as LED indicators, screen brightness, shutter sounds, WLAN, etc.  
These Broadcast Intent can be sent directly from the plugin app, or by using simple wrapper methods provided by [RICOH THETA Plugin Library](https://github.com/ricohapi/theta-plugin-library). In addition, [RICOH THETA Plugin SDK](https://github.com/ricohapi/theta-plugin-sdk/releases) includes sample code demonstrating how to call these methods.  

### Contents

* [Receive Key Evernt](#receive-key-event)
* [Disable Power Button Feature](#disable-power-button-feature)
* [Control the LEDs](#control-the-leds)
* [Control the OLED](#control-the-oled)
* [Control the LEDs and OLED Brightness](#control-the-leds-and-oled-brightness)
* [Control the LED and Screen Brightness](#control-the-led-and-screen-brightness)
* [Sound Effect](#sound-effect)
* [Control WLAN](#control-wlan)
* [Control Bluetooth](#control-bluetooth)
* [Control GPS](#control-gps)
* [Control IMU](#control-imu)
* [Control Battery Charging](#control-battery-charging)
* [Power Off](#power-off)
* [Add File to the Media Database](#add-file-to-the-media-database)
* [Notify on Error Occurrence](#notify-on-error-occurrence)
* [Notify Plugin Termination](#notify-plugin-termination)
* [Notify Camera Resource Control Change](#notify-camera-resource-control-change)

## Receive Key Event

#### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) |
|:-:|:-:|:-:|
|   | ✓ | ✓ |

When a camera button is pressed or released, a Broadcast Intent  is sent. The mapping between button actions and corresponding Broadcast Intent is shown below.

| Broadcast Intent | Description | 
|:--|:--|
| `com.theta360.plugin.ACTION_KEY_DOWN` | Button is Pressed |
| `com.theta360.plugin.ACTION_KEY_UP`   | Button is Released |

The button type (pressed or released) is included in the extra data of the Broadcast Intent, as listed below.  

| Key | Type | Description |
|:--|:--|:--|
| `keyCode` | Int | `26`: Power Button<br>`27`: Shutter Button<br>`130`: Mode Button<br>`284`: WLAN Button<br>`119`: Fn Button<sup>\*1</sup>|
| `KeyEvent` | KeyEvent | KeyEvent object received from Android framework |

<sup>\*1</sup> THETA Z1 only  

## Disable Power Button Feature

#### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) |
|:-:|:-:|:-:|
| ✓<sup>\*1</sup> | ✓<sup>\*2</sup> ||

<sup>\*1</sup> RICOH THETA X firmware v1.40.0 and later  
<sup>\*2</sup> RICOH THETA Z1 firmware v2.10.3 and later  

The plugin can disable the power button functionality that puts the device into sleep mode or powers it off.
Even when disabled, the plugin can still receive the key event with `KEYCODE_POWER` (26).

| Broadcast Intent | Description | 
|:--|:--|
| `com.theta360.plugin.ACTION_ENABLE_POWER_BUTTON`  | Enable power button feature |
| `com.theta360.plugin.ACTION_DISABLE_POWER_BUTTON` | Disable power button feature |

## Control the LEDs

#### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) |
|:-:|:-:|:-:|
|   |   | ✓ |

### Turn on LEDs

Plugins can control the camera's LEDs, including LED3, LED4, LED5, LED6, LED7, and LED8 (turn on / blink / turn off).  
To turn on an LED using a Broadcast Intent, use the action `com.theta360.plugin.ACTION_LED_SHOW`.  

The following extra data must be included in the Intent:  

| Key | Type | Description |
|:--|:--|:--|
| `target` | String | Choose from `"LED3"`, `"LED4"`, `"LED5"`, `"LED6"`, `"LED7"`, `"LED8"` |
| `color`  | String | Choose from `"blue"`, `"green"`, `"red"`, `"cyan"`, `"magenta"`, `"yellow"`, `"white"`. Default is `"blue"`. |

When this Broadcast Intent is used, the LED control will be executed regardless of its current state. The LED will be reset and lit according to the requested parameters.  

#### Sample
```java
Intent intent = new Intent("com.theta360.plugin.ACTION_LED_SHOW");
intent.putExtra("target", "LED3");
intent.putExtra("color",  "blue");
sendBroadcast(intent);   
```

#### Method by Plugin Library
```java
notificationLed3Show(LedColor.BLUE);
```

### Blink LEDs

To make an LED blink using a Broadcast Intent, use the action `com.theta360.plugin.ACTION_LED_BLINK`.  

The following extra data must be included in the Intent:  

| Key | Type | Description |
|:--|:--|:--|
| `target` | String | Choose from `"LED3"`, `"LED4"`, `"LED5"`, `"LED6"`, `"LED7"`, `"LED8"` |
| `color`  | String | Choose from `"blue"`, `"green"`, `"red"`, `"cyan"`, `"magenta"`, `"yellow"`, `"white"`. Default is `"blue"`. |
| `period` | Int | 1-2000 [msec]. Default is 2000. |

When this Broadcast Intent is used, the LED will be reset and start blinking based on the specified parameters, regardless of its current state (on or off).  

#### Sample
```java
Intent intent = new Intent("com.theta360.plugin.ACTION_LED_BLINK");
intent.putExtra("target", "LED3");
intent.putExtra("color",  "blue");
intent.putExtra("period", 250);
sendBroadcast(intent);
```
#### Method by Plugin Library

```java
notificationLedBlink("LED3", "blue", 250);
```

### Turn off LEDs

To turn off an LED using a Broadcast Intent, use the action `com.theta360.plugin.ACTION_LED_HIDE`.  

The following extra data must be included in the Intent:  

| Key | Type | Description |
|:--|:--|:--|
| `target` | String | Choose from `"LED3"`, `"LED4"`, `"LED5"`, `"LED6"`, `"LED7"`, `"LED8"` |

When this Broadcast Intent is used, the LED will be reset and turned off according to the specified parameters, regardless of its current state (on or off).  

#### Sample
```java
Intent intent = new Intent("com.theta360.plugin.ACTION_LED_HIDE");
intent.putExtra("target", "LED3");
sendBroadcast(intent);
```

#### Method by Plugin Library
```java
notificationLedHide("LED3");
```

## Control the OLED

#### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) |
|:-:|:-:|:-:|
|   | ✓ |   |

### Set Display Mode

To switch between plugin mode display and basic display on the OLED, use the Broadcast Intent `com.theta360.plugin.ACTION_OLED_DISPLAY_SET`.

| Key | Type | Description |
|:--|:--|:--|
| `display` | String | Choose from `"plugin"`, `"basic"` |

To use the following Broadcast Intent, set the display mode to `"plugin"`.  

* `com.theta360.plugin.ACTION_OLED_IMAGE_SHOW`
* `com.theta360.plugin.ACTION_OLED_IMAGE_BLINK`
* `com.theta360.plugin.ACTION_OLED_TEXT_SHOW`
* `com.theta360.plugin.ACTION_OLED_HIDE`

When the display mode is switched from `"basic"` display to `"plugin"` mode display, the plugin name is shown in OLED.  

#### Sample
```java
Intent intent = new Intent("com.theta360.plugin.ACTION_OLED_DISPLAY_SET");
intent.putExtra("display", "plugin");
sendBroadcast(intent);
```

#### Method by Plugin Library
```java
notificationOledDisplaySet("plugin");
```

### Display Bitmap Image

To display an bitmap image on the OLED, use the Broadcast Intent `com.theta360.plugin.ACTION_OLED_IMAGE_SHOW`.

On firmware version 1.20.1 and later, bitmap images can be displayed on the full OLED area (128x36). On earlier versions, only the lower two-thirds (128x24) of the OLED is used for image display.  

The following extra data must be included in the Intent:  

| Key | Type | Description |
|:--|:--|:--|
| `bitmap` | Bitmap | Bitmap image (128x24 or 128x36) |

When this Broadcast Intent is used, any existing OLED display (including blinking content) will be cleared, and the specified image will be shown.  

#### Sample
```java
// Bitmap size is height 24 or 36 and width 128
Bitmap image = Bitmap.createBitmap(128, 24, Bitmap.Config.ARGB_8888);//All black image

Intent intent = new Intent(com.theta360.plugin.ACTION_OLED_IMAGE_SHOW);
intent.putExtra(bitmap, image);
sendBroadcast(intent);
```

#### Method by Plugin Library
```java
Bitmap image = Bitmap.createBitmap(128, 24, Bitmap.Config.ARGB_8888 );//All black image

notificationOledImageShow(image);
```

### Blink Bitmap Image

To make the OLED flash an image, use the Broadcast Intent `com.theta360.plugin.ACTION_OLED_IMAGE_BLINK`.  

On firmware version 1.20.1 and later, bitmap images can be displayed on the full OLED area (128x36). On earlier versions, only the lower two-thirds (128x24) of the OLED is used for image display.  

The following extra data must be included in the Intent:  

| Key | Type | Description |
|:--|:--|:--|
| `bitmap` | Bitmap | Bitmap image (128x24 or 128x36) |
| `period` | Int    | 250-2000 [msec]. Default is 2000. |

When this Broadcast Intent is used, any existing OLED display (including blinking content) will be cleared, and the specified image will start blinking.  

#### Sample
```java
//Bitmap size is height 24 or 36 and width 128
Bitmap image = Bitmap.createBitmap(128, 24, Bitmap.Config.ARGB_8888 );//All black image

Intent intent = new Intent(com.theta360.plugin.ACTION_OLED_IMAGE_BLINK);
intent.putExtra(bitmap, image);
intent.putExtra(period, 250);
sendBroadcast(intent);
```

#### Method by Plugin Library
```java
Bitmap image = Bitmap.createBitmap(128, 24, Bitmap.Config.ARGB_8888 );//All black image

notificationOledImageBlink(image, 250);
```

### Display Characters

To display text on the OLED, use the Broadcast Intent `com.theta360.plugin.ACTION_OLED_TEXT_SHOW`.  

Text can be displayed in the lower one-third (128x12) or middle one-third (128x12) area of the OLED. The following extra data must be included in the Intent.  

On firmware version 1.20.1 and later, it is also possible to display text in the top one-third area (128x12).  

| Key | Type | Description |
|:--|:--|:--|
| `text-top`    | String | ASCII printable characters (0x20-0x7E) |
| `text-middle` | String | ASCII printable characters (0x20-0x7E) |
| `text-bottom` | String | ASCII printable characters (0x20-0x7E) |

Text set for the middle area is displayed where the plugin name normally appears, while text set for the lower area is shown in the blank region.  

To remove displayed text, specify an empty string (`""`) for the value.  

When this Broadcast Intent is used, only the portion corresponding to the specified key is updated, and the text display begins accordingly.  

#### Sample
```java
Intent intent = new Intent(Constants.ACTION_OLED_TEXT_SHOW);
intent.putExtra("text-middle", "This is a sample characters");
sendBroadcast(intent);
```

#### Method by Plugin Library
```java
Map<TextArea, String> output = new HashMap<>() ;
output.put(TextArea.TOP, "This is a sample characters to top area.");
output.put(TextArea.MIDDLE, "This is a sample characters to middle area.");
output.put(TextArea.BOTTOM, "This is a sample characters to bottom area.");
notificationOledTextShow(output);
```

### Turn Off

To turn off the OLED, use the Broadcast Intent `com.theta360.plugin.ACTION_OLED_HIDE`.  

When this Broadcast Intent is used, the OLED will turn off immediately, regardless of whether it is currently on or blinking.  

#### Sample
```java
sendBroadcast(new Intent("com.theta360.plugin.ACTION_OLED_HIDE"));
```

#### Method by Plugin Library
```java
notificationOledHide();
```

## Control the LED and Screen Brightness

### Set LED and OLED Brightness

#### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) |
|:-:|:-:|:-:|
| ✓ | ✓ | ✓ |

To adjust the brightness of the LEDs or the OLED, use the Broadcast Intent `com.theta360.plugin.ACTION_LED_BRIGHTNESS_SET`.  

The following extra data must be included in the Intent:  

| Key | Type | Description |
|:--|:--|:--|
| `target` | String | **RICOH THETA V**<br>Choose from `"LED1"`, `"LED2"`, `"LED3"`, `"LED4"`, `"LED5"`, `"LED6"`, `"LED7"`, `"LED8"`<br><br>**RICOH THETA Z1**<br>Choose from `"LED1"`, `"LED2"`, `"OLED"`<br><br>**RICOH THETA X**<br>Choose from `"LED1"`, `"LED2"` |
| `brightness` | Int<sup>\*1</sup> | 0-100[%]. Default is 25. |

<sup>\*1</sup> In THETA X firmware v1.10.1 and earlier, there is a known issue where the value must be specified as a String.

#### Sample
```java
 Intent intent = new Intent("com.theta360.plugin.ACTION_LED_BRIGHTNESS_SET");
 intent.putExtra("target", "OLED");
 intent.putExtra("brightness", 25);
 sendBroadcast(intent);
```

#### Method by Plugin Library
```java
notificationLedBrightnessSet("OLED", 25);
```

## Set the Screen Brightness

#### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) |
|:-:|:-:|:-:|
| ✓ ||| 

### Setting Brightness

To adjust the screen brightness, use the Broadcast Intent 
`com.theta360.plugin.ACTION_SCREEN_BRIGHTNESS_SET`.  

The following extra data must be included in the Intent:  

| Key | Type | Description |
|:--|:--|:--|
| `brightness` | Int | 0-100[%]. Default is 25. |

> [!NOTE]  
> Even if the brightness is set to `0`, the screen backlight is not completely turned off.  

#### Sample
```java
Intent intent = new Intent("com.theta360.plugin.ACTION_SCREEN_BRIGHTNESS_SET");
intent.putExtra("brightness", 100);
sendBroadcast(intent);
```

#### Method by Plugin Library
```java
notificationScreenBrightnessSet(100);
```

## Sound Effect

Plugins can playback the THETA built-in sound effect via Broadcast Intent.  

| Broadcast Intent | Description |
|:--|:--|
| `com.theta360.plugin.ACTION_AUDIO_SHUTTER` | Shutter sound |
| **RICOH THETA V, Z1**<br>`com.theta360.plugin.ACTION_AUDIO_SH_OPEN`<br><br>**RICOH THETA X**<br>`com.theta360.plugin.ACTION_AUDIO_SHUTTER_OPEN`| Long shutter start sound |
| **RICOH THETA V, Z1**<br>`com.theta360.plugin.ACTION_AUDIO_SH_CLOSE`<br><br>**RICOH THETA X**<br>`com.theta360.plugin.ACTION_AUDIO_SHUTTER_CLOSE` | Long shutter end sound |
| **RICOH THETA V, Z1**<br>`com.theta360.plugin.ACTION_AUDIO_MOVSTART`<br><br>**RICOH THETA X**<br>`com.theta360.plugin.ACTION_AUDIO_MOVIE_START` | Video Recording start sound |
| **RICOH THETA V, Z1**<br>`com.theta360.plugin.ACTION_AUDIO_MOVSTOP`<br><br>**RICOH THETA X**<br>`com.theta360.plugin.ACTION_AUDIO_MOVIE_STOP` | Video Recording stop sound |
| `com.theta360.plugin.ACTION_AUDIO_SELF` | Self timer Pi sound |
| `com.theta360.plugin.ACTION_AUDIO_WARNING` | Warning Pi-Pi-Pi sound |

#### Sample
```java
sendBroadcast(new Intent("com.theta360.plugin.ACTION_AUDIO_SHUTTER"));
```

#### Method by Plugin Library
```java
notificationAudioShutter();
```

## Control WLAN

#### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) |
|:-:|:-:|:-:|
| ✓ | ✓ | ✓ |

WLAN operation can be managed using Broadcast Intents corresponding to each WLAN mode.  

> [!WARNING]  
> If a developer registration AP restriction is applied, switching to CL mode is not permitted.  

| Broadcast Intent | Description |
|:--|:--|
| `com.theta360.plugin.ACTION_WLAN_OFF` | OFF |
| `com.theta360.plugin.ACTION_WLAN_AP`  | AP mode |
| `com.theta360.plugin.ACTION_WLAN_CL`  | CL mode |

#### Sample
```java
sendBroadcast(new Intent("com.theta360.plugin.ACTION_WLAN_OFF"));
```

#### Method by Plugin Library
```java
notificationWlanOff();
notificationWlanAp();
notificationWlanCl();
```

## Control Bluetooth

#### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) |
|:-:|:-:|:-:|
| ✓<sup>\*1</sup> ||| 

<sup>\*1</sup>THETA X firmware v2.00.0 and later.  

| Broadcast Intent | Description |
|:--|:--|
| `com.theta360.plugin.ACTION_BLUETOOTH_OFF` | Turn off |
| `com.theta360.plugin.ACTION_BLUETOOTH_ON`  | Turn on |

#### Method by Plugin Library
```java
notificationBluetoothOff();
notificationBluetoothOn();
```

## Control GPS

#### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) |
|:-:|:-:|:-:|
| ✓<sup>\*1</sup> ||| 

<sup>\*1</sup>THETA X firmware v2.00.0 and later.  

| Broadcast Intent | Description |
|:--|:--|
| `com.theta360.plugin.ACTION_GPS_TAG_RECORDING_OFF` | Turn off |
| `com.theta360.plugin.ACTION_GPS_TAG_RECORDING_ON`  | Turn on |

#### Method by Plugin Library
```java
notificationGpsOff();
notificationGpsOn();
```

## Control IMU

#### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) |
|:-:|:-:|:-:|
|   | ✓ | ✓ |

The IMU can be turned on or off using the following Broadcast Intent. Turning on the IMU is required to perform zenith correction when the plugin uses the Camera API.  

| Broadcast Intent | Description |
|:--|:--|
| `com.theta360.plugin.ACTION_MOTION_SENSOR_STOP`  | Stop IMU  |
| `com.theta360.plugin.ACTION_MOTION_SENSOR_START` | Start IMU |

#### Method by Plugin Library
```java
notificationSensorStop();
notificationSensorStart();
```

## Control Battery Charging

#### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) |
|:-:|:-:|:-:|
| ✓<sup>\*1</sup> ||| 

<sup>\*1</sup>THETA X firmware v2.20.1 and later.  

Battery charging can be suspended or resumed using the following Broadcast Intent.  

> [!WARNING]  
> If the battery level is near 0%, the camera may power off shortly after sending `ACTION_BATTERY_CHARGING_RESUME`.

| Broadcast Intent | Description |
|:--|:--|
| `com.theta360.plugin.ACTION_BATTERY_CHARGING_SUSPEND`  | Suspend Battery Charging |
| `com.theta360.plugin.ACTION_BATTERY_CHARGING_RESUME` | Resume Battery Charging |

#### Method by Plugin Library
```java
notificationBatteryChargingSuspend();
notificationBatteryChargingResume();
```

## Power Off

#### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) |
|:-:|:-:|:-:|
| ✓<sup>\*1</sup> ||| 

<sup>\*1</sup>THETA X firmware v2.30.0 and later.  

To power off the THETA, use the following Broadcast Intent.  

| Broadcast Intent | Description |
|:--|:--|
| `com.theta360.plugin.ACTION_POWER_OFF` | Power Off |

#### Method by Plugin Library
```java
notificationPowerOff();
```

## Add File to the Media Database

#### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) |
|:-:|:-:|:-:|
| ✓ | ✓ | ✓ | 

By adding image files captured by the plugin to the media database, they can be accessed via USB-MTP and listed using the `camera.listFiles` Web API. To achieve this, the Broadcast Intent `com.theta360.plugin.ACTION_DATABASE_UPDATE` can be used.  

The following extra data must be included in the Intent:  

### RICOH THETA V / Z1

| Key | Type | Description |
|:--|:--|:--|
| `targets` | String Array | Array of directory path or file path<br><br>**Example**<br>`["DCIM/100RICOH/R0010001.JPG","DCIM/101RICOH"]` |

Use the `targets` parameter to specify the file(s) to be updated. If a directory is specified, all files under that directory will be updated.  

Specify the path starting from the /sdcard/DCIM directory, as shown below. Paths are case-insensitive, so uppercase and lowercase letters can be used.  

#### Sample
```java
Intent intent = new Intent("com.theta360.plugin.ACTION_DATABASE_UPDATE");
intent.putExtra("targets", "DCIM/100RICOH/R0010001.JPG");
sendBroadcast(intent);
```

#### Method by Plugin Library
```java
notificationDatabaseUpdate("DCIM/100RICOH/R0010001.JPG");
```

### RICOH THETA X  

| Key | Type | Description |
|:--|:--|:--|
| `target` | String | Full path of file<br><br>**Example**<br>For internal memory, `"storage/emulated/0/DCIM/100_TEST/R0000001.MP4"`<br>For microSD cards, `"storage/BSC8-1948/DCIM/100_TEST/R0000001.MP4"` |

Only a full file path can be specified for `target`. Folders and multiple files are not supported.  

In addition, folder and file names must comply with DCF rules, and media files must be in equirectangular format. 8K videos are not supported — files must be compatible with playback in the camera UI.  

#### Sample
```java
Intent intent = new Intent("com.theta360.plugin.ACTION_DATABASE_UPDATE");
intent.putExtra("target", "storage/emulated/0/DCIM/100_TEST/R0000001.MP4");
sendBroadcast(intent);
```

#### Method by Plugin Library
```java
notificationDatabaseUpdate("storage/emulated/0/DCIM/100_TEST/R0000001.MP4");
```

## Notify on Error Occurrence

#### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) |
|:-:|:-:|:-:|
|   | ✓ | ✓ | 

When the Broadcast Intent `com.theta360.plugin.ACTION_ERROR_OCCURRED` is used, a notification indicating that an error has occurred in the plugin will be sent.  
Upon receiving this notification, the camera plays a warning tone and blinks LED2 in red.  

#### Sample
```java
sendBroadcast(new Intent("com.theta360.plugin.ACTION_ERROR_OCCURED"));
```

#### Method by Plugin Library
```java
notificationErrorOccured();
```

## Notify Plugin Termination

When the Broadcast Intent `com.theta360.plugin.ACTION_FINISH_PLUGIN` is used, a notification indicating that the plugin has finished will be sent.  

The following extra data must be included in the Intent:  

| Key | Type | Description |
|:--|:--|:--|
| `packageName` | String | Package name |
| `exitStatus`  | String | `"success"` or `"failure"`.<br>If set to `"failure"`, a warning tone will be played and LED2 will blink red. |
| `message` | String | Optional |

On RICOH THETA X, this Intent must NOT be sent when the plugin exits.  

#### Sample
```java
Intent intent = new Intent("com.theta360.plugin.ACTION_FINISH_PLUGIN");
intent.putExtra("packageName", "The name of the package you are creating.");
intent.putExtra("exitStatus", "success");
sendBroadcast(intent);
```

#### Method by Plugin Library
```java
notificationSuccess();
notificationError("some kind of message");
```

## Notify Camera Resource Control Change

#### Supported Models
| ![X](https://img.shields.io/badge/X-purple) | ![Z1](https://img.shields.io/badge/Z1-blue) | ![V](https://img.shields.io/badge/V-green) |
|:-:|:-:|:-:|
| ✓ | ✓ | ✓ | 

### RICOH THETA V / Z1

When the Broadcast Intent `com.theta360.plugin.ACTION_MAIN_CAMERA_CLOSE` is used, it notifies that the plugin is taking control of the camera resources. After this, the controlling camera via [Camera API](./camera-api.md) becomes available for use.  

#### Sample
```java
sendBroadcast(new Intent("com.theta360.plugin.ACTION_MAIN_CAMERA_CLOSE"));
```

#### Method by Plugin Library
```java
notificationCameraClose();
```

When the Broadcast Intent `com.theta360.plugin.ACTION_MAIN_CAMERA_OPEN` is used, it notifies that the plugin has released the camera resources. After this, the controlling camera via [Camera API](./camera-api.md) will no longer be available.  

#### Sample
```java
sendBroadcast(new Intent("com.theta360.plugin.ACTION_MAIN_CAMERA_OPEN"));
```

#### Method by Plugin Library
```java
notificationCameraOpen();
```

### RICOH THETA X  
To enable shooting via the Web API, use the Broadcast Intent `com.theta360.plugin.ACTION_PLUGIN_WEBAPI_CAMERA_OPEN`. After this, the controlling camera via [Camera API](./camera-api.md) will no longer be available.  

#### Sample
```java
sendBroadcast(new Intent("com.theta360.plugin.ACTION_PLUGIN_WEBAPI_CAMERA_OPEN"));
```

#### Method by Plugin Library
```java
notificationWebApiCameraOpen();
```

When shooting is finished via the Web API (i.e., when closing the plugin), use `com.theta360.plugin.ACTION_PLUGIN_WEBAPI_CAMERA_CLOSE`.  

#### Sample
```java
sendBroadcast(new Intent("com.theta360.plugin.ACTION_PLUGIN_WEBAPI_CAMERA_CLOSE"));
```

#### Method by Plugin Library
```java
notificationWebApiCameraClose();
```
