# Broadcast Intent

Plugin can send Broadcast Intent to control several hardware feature, such as controlling LED and Screen brightness, shutter sounds, WLAN, etc.

### Contents

* [Supported by Plugin Library](#supported-by-plugin-library)
* [Receiving Button Events](#receiving-button-events)
* [Disable Power Button Feature](#disable-power-button-feature)
* [Control the LEDs](#control-the-leds)
* [Control the OLED](#control-the-oled)
* [Control the LEDs and OLED Brightness](#control-the-leds-and-oled-brightness)
* [Control the Screen Brightness](#control-the-screen-brightness)
* [Sound Effect](#sound-effect)
* [Control WLAN](#control-wlan)
* [Control Bluetooth](#control-bluetooth)
* [Control GPS](#control-gps)
* [Control IMU Sensor](#control-imu-sensor)
* [Control Battery Charging](#control-battery-charging)
* [Updating the Database](#updating-the-database)
* [Notifying Occurrences of Errors](#notifying-occurrences-of-errors)
* [Notifying Completion of Plugin](#notifying-completion-of-plugin)
* [Notifying Camera Device Control](#notifying-camera-device-control)

## Supported by Plugin Library

Broadcast Intent features can be sent by plugin app directly, and they are provided as simple methods too by [Plugin Library](https://github.com/ricohapi/theta-plugin-library). Also, [Plugin SDK](../ricoh-theta-plugin/sdk.md) provides some sample code to call these methods.

## Receiving Button Events

When the camera button is pressed down or pushed up, Broadcast Intent is set. Combinations of button operation and the intent are as follows:

|Button Operation|Intent|
|:-|:-|
|Pushed down|(RICOH THETA V, Z1) <br/> "com.theta360.plugin.ACTION_KEY_DOWN"|
|Pushed up|(RICOH THETA V, Z1) <br/> "com.theta360.plugin.ACTION_KEY_UP"|

The button type when pressed down or pushed up is listed below in the Broadcast Intent extension data:

|Key|Type|Description|
|:-|:-|:-|
|"keyCode"|int|(RICOH THETA V) <br/> 27: Shutter Button, 130: Mode Button, 284: Wireless Button can be specified <br/><br/> (RICOH THETA Z1) <br/> 27: Shutter Button, 119: Fn Button, 130: Mode Button, 284: Wireless Button can be specified <br/><br/> (RICOH THETA X) <br/> 27: Shutter Button, 130: Mode Button can be specified|
|"KeyEvent"|KeyEvent|KeyEvent object received from OS|

## Disable Power Button Feature

Plugin can disable power button feature to enter to sleep mode, and to power off the device. Even if disabling it, plugin can receive the key event with KEYCODE_POWER (26). This Broadcast Intent is available with RICOH THETA X firmware v1.40.0 and RICOH THETA Z1 firmware v2.10.3 or later.

|Intent|Description|
|:-|:-|
|com.theta360.plugin.ACTION_ENABLE_POWER_BUTTON | enable power button feature(default)|
|com.theta360.plugin.ACTION_DISABLE_POWER_BUTTON|disable power button feature|

## Control the LEDs

The following functionality is for RICOH THETA V.  
RICOH THETA Z1 and X only support Setting Brightness.

Plugins can control LEDs on the camera including LED3, LED4, LED5, LED6, LED7, LED8 (turn on / blink / turn off).

### Turning on LEDs

When using "com.theta360.plugin.ACTION_LED_SHOW" with Broadcast Intent, the LED will light up. When using Broadcast Intent, the following extension data must be set:

|Key|Type|Description|
|:-|:-|:-|
|target|String|Choose from "LED3", "LED4", "LED5", "LED6", "LED7", "LED8"|
|color|String|Choose from "blue", "green", "red", "cyan", "magenta", "yellow", "white". Default is "blue".|

With target, set the target LED to be turned on. If target is not specified, Broadcast Intent is ignored. With color, set the luminescent color. Valid only when target is set to LED3.

When Broadcast Intent is used, whether the target LED is already on or already off, processing the LED will be cancelled and start with the requested lighting.

When the THETA Plugin library is not used:
```
Intent intent = new Intent("com.theta360.plugin.ACTION_LED_SHOW");
intent.putExtra("target", "LED3");
intent.putExtra("color",  "blue");
sendBroadcast(intent);   
```
When using the THETA Plugin library:
```
notificationLed3Show( LedColor.BLUE );
```

### Blinking LEDs

When using "com.theta360.plugin.ACTION_LED_BLINK" with Broadcast Intent, the LED will blink. When using Broadcast Intent, the following extension data must be set:

|Key|Type|Description|
|:-|:-|:-|
|target|String|Choose from "LED3", "LED4", "LED5", "LED6", "LED7", "LED8"|
|color|String|Choose from "blue", "green", "red", "cyan", "magenta", "yellow", "white". Default is "blue".|
|period|int|1-2000 (msec). Default is 2000.|

With target, set the target LED to blink. If target is not specified, Broadcast Intent is ignored. With color, set the luminescent color. Valid only when target is set to LED3. Use period to set 1 cycle time period.

When Broadcast Intent is used, whether the target LED is already on or already off, processing the LED will be cancelled and start with the requested lighting.

When the THETA Plugin library is not used:
```
Intent intent = new Intent("com.theta360.plugin.ACTION_LED_BLINK");
intent.putExtra("target", "LED3");
intent.putExtra("color",  "blue");
intent.putExtra("period", "250");
sendBroadcast(intent);
```
When using the THETA Plugin library:
```
notificationLedBlink("LED3", "blue", "250");
```

### Turning off LEDs

When using "com.theta360.plugin.ACTION_LED_HIDE" with Broadcast Intent, the LED will turn off. When using Broadcast Intent, the following extension data must be set:

|Key|Type|Description|
|:-|:-|:-|
|target|String|Choose from "LED3", "LED4", "LED5", "LED6", "LED7", "LED8"|

When Broadcast Intent is used, whether the target LED is already on or already off, processing the LED will be cancelled and start with the requested lighting.

With target, set target LED to turn off. If target is not specified, Broadcast Intent is ignored. When Broadcast Intent is used, whether the target LED is already on or already off, processing the LED will be cancelled and start with the requested lighting.

When the THETA Plugin library is not used:
```
Intent intent = new Intent("com.theta360.plugin.ACTION_LED_HIDE");
intent.putExtra("target", "LED3");
sendBroadcast(intent);
```
When using the THETA Plugin library:
```
notificationLedHide("LED3");
```

## Control the OLED

The following functionality is for RICOH THETA Z1.

Plugins can control the OLED.

### Displaying Images 

By setting Broadcast Intent to "com.theta360.plugin.ACTION_OLED_IMAGE_SHOW" you can display images on the OLED.

Images are displayed in the lower 2/3 area (128x24) of the OLED. Extended data is mandatory for Broadcast Intent below.

Firmware Ver 1.20.1 or later, the entire OLED (128x36) can now display bitmap images.

|Key|Type|Description|
|:-|:-|:-|
|bitmap|Bitmap|128x24 or 128x36 Bitmap|

Specify the image to be displayed with bitmap. If no image is specified, or if the size is not 128x24 or 128x36 Broadcast Intent will be ignored.

When using Broadcast Intent, regardless of whether the OLED is already on or blinking, processing stops and the specified image is displayed.

When the THETA Plugin library is not used:
```
// Bitmap size is height 24 or 36 and width 128
Bitmap image = Bitmap.createBitmap(128, 24, Bitmap.Config.ARGB_8888 );//All black image

Intent intent = new Intent(com.theta360.plugin.ACTION_OLED_IMAGE_SHOW);
intent.putExtra(bitmap, image);
sendBroadcast(intent);
```
When using the THETA Plugin library:
```
Bitmap image = Bitmap.createBitmap(128, 24, Bitmap.Config.ARGB_8888 );//All black image

notificationOledImageShow(image);
```

### Flashing Image

By setting broadcast intent to "com.theta360.plugin.ACTION_OLED_IMAGE_BLINK" you can set it to flash images on the OLED. 

Images are displayed in the lower 2/3 area (128x24) of the OLED. Extended data is mandatory for the broadcast intent below.

Firmware Ver 1.20.1 or later, the entire OLED (128x36) can now display bitmap images.

|Key|Type|Description|
|:-|:-|:-|
|bitmap|Bitmap|128x24 or 128x36 Bitmap|
|period|Integer|250-2000 (msec). Default is 2000.|

Specify the image to be displayed with bitmap. If no image is specified, or if the size is not 128x24 or 128x36, Broadcast Intent will be ignored.

When using Broadcast Intent, regardless of whether the OLED is already on or blinking, processing stops and the specified image is displayed.

When the THETA Plugin library is not used:
```
//Bitmap size is height 24 or 36 and width 128
Bitmap image = Bitmap.createBitmap(128, 24, Bitmap.Config.ARGB_8888 );//All black image

Intent intent = new Intent(com.theta360.plugin.ACTION_OLED_IMAGE_BLINK);
intent.putExtra(bitmap, image);
intent.putExtra(period, 250);
sendBroadcast(intent);
```
When using the THETA Plugin library:
```
Bitmap image = Bitmap.createBitmap(128, 24, Bitmap.Config.ARGB_8888 );//All black image

notificationOledImageBlink(image, 250);
```

### Displaying Characters

By setting Broadcast Intent to "com.theta360.plugin.ACTION_OLED_TEXT_SHOW" you can display characters on the OLED.

Characters are displayed in the lower 1/3 area (128x12) or in the middle 1/3 area (128x12). Extended data is mandatory for Broadcast Intent below.

From firmware Ver 1.20.1, it is possible to display in the top 1/3 area (128x12).

|Key|Type|Description|
|:-|:-|:-|
|text-top|String|ASCII printable characters (32 - 126)|
|text-middle|String|ASCII printable characters (32 - 126)|
|text-bottom|String|ASCII printable characters (32 - 126)|

Characters set as middle display characters are displayed in the plugin name area. Characters set as lower display characters are displayed in the blank area.

The displayed text can be deleted by specifying "".   

When Broadcast Intent is used, only the part corresponding to the specified key is rewritten and displaying is started.

When the THETA Plugin library is not used:
```
Intent intent = new Intent(Constants.ACTION_OLED_TEXT_SHOW);
intent.putExtra("text-middle", "This is a sample characters");
sendBroadcast(intent);
```
When using the THETA Plugin library:
```
Map<TextArea, String> output = new HashMap<>() ;
output.put(TextArea.TOP, "This is a sample characters to top area.");
output.put(TextArea.MIDDLE, "This is a sample characters to middle area.");
output.put(TextArea.BOTTOM, "This is a sample characters to bottom area.");
notificationOledTextShow(output);
```

### OLED Turns Off

By setting Broadcast Intent to "com.theta360.plugin.ACTION_OLED_HIDE" you can turn off the OLED.

When using Broadcast Intent, regardless of whether the OLED is already on or blinking, processing stops and the OLED turns off.

When the THETA Plugin library is not used:
```
sendBroadcast(new Intent("com.theta360.plugin.ACTION_OLED_HIDE"));
```
When using the THETA Plugin library:
```
notificationOledHide();
```

### Display Method Settings

By setting Broadcast Intent to "com.theta 360.plugin.ACTION_OLED_DISPLAY_SET" the plugin mode display or basic display can be set. Extended data is mandatory for Broadcast Intent below.

|Key|Type|Description|
|:-|:-|:-|
|display|String|Choose from "plugin", "basic"|

If display is not specified, Broadcast Intent will be ignored. When the display method is set to basic display, the following Broadcast Intent is ignored:

* "com.theta360.plugin.ACTION_OLED_IMAGE_SHOW"
* "com.theta360.plugin.ACTION_OLED_IMAGE_BLINK"
* "com.theta360.plugin.ACTION_OLED_TEXT_SHOW"
* "com.theta360.plugin.ACTION_OLED_HIDE"

When the display method is changed from basic display to plugin mode display, the plugin name is displayed in the plugin name area.

When the THETA Plugin library is not used:
```
Intent intent = new Intent("com.theta360.plugin.ACTION_OLED_DISPLAY_SET");
intent.putExtra("display", "basic");
sendBroadcast(intent);
```
When using the THETA Plugin library:
```
notificationOledDisplaySet("basic");
```
## Control the LEDs and OLED Brightness

### Setting Brightness

By setting Broadcast Intent to "com.theta360.plugin.ACTION_LED_BRIGHTNESS_SET" you can set the brightness of LED's and the OLED. Extended data is mandatory for Broadcast Intent below.

|Key|Type|Description|
|:-|:-|:-|
|target|String| (RICOH THETA V) <br/>Choose from "LED1", "LED2", "LED3", "LED4", "LED5", "LED6", "LED7", "LED8"<br/><br/>(RICOH THETA Z1) <br/>Choose from "LED1", "LED2", "OLED"<br/><br/>(RICOH THETA X) <br/>Choose from "LED1", "LED2" |
|brightness|Integer(V/Z1)<br/>String(X)|0-100(%).Default is 25.|

Set the target LED's brightness to change with target. If target is not specified, Broadcast Intent will be ignored.

Set the brightness value with brightness. If brightness is not specified, Broadcast Intent will be ignored.

When the THETA Plugin library is not used:

*You can set the brightness of LED's as well as OLED.

```
 Intent intent = new Intent("com.theta360.plugin.ACTION_LED_BRIGHTNESS_SET");
 intent.putExtra("target", "OLED");
 intent.putExtra("brightness", "25");
 sendBroadcast(intent);
```
When using the THETA Plugin library:
```
notificationLedBrightnessSet("OLED", 25);
```

## Control the Screen Brightness

The following functionality is for RICOH THETA X.  

### Setting Brightness

By setting Broadcast Intent to "com.theta360.plugin.ACTION_SCREEN_BRIGHTNESS_SET" you can set the brightness of Screen. Extended data is mandatory for Broadcast Intent below.

|Key|Type|Description|
|:-|:-|:-|
|brightness|Integer<br/>String|0-100(%).Default is 25.|

Set the brightness value with brightness. If brightness is not specified, Broadcast Intent will be ignored.  
Even when brightness is set to 0%, the screen backlighting is not turned off completely.  

When the THETA Plugin library is not used:
```
Intent intent = new Intent("com.theta360.plugin.ACTION_SCREEN_BRIGHTNESS_SET");
intent.putExtra("brightness", "100");
sendBroadcast(intent);
```
When using the THETA Plugin library:
```
notificationScreenBrightnessSet(100);
```

## Sound Effect

Plugins can use the camera's audio files. Using Broadcast Intent for each audio file you can play audio files.

|Audio File|Intent|
|:-|:-|
|Shutter Audio|"com.theta360.plugin.ACTION_AUDIO_SHUTTER"|
|Shutter Audio Start|(RICOH THETA V, Z1) <br/> "com.theta360.plugin.ACTION_AUDIO_SH_OPEN"<br/><br/>(RICOH THETA X) <br/> "com.theta360.plugin.ACTION_AUDIO_SHUTTER_OPEN"|
|Shutter Audio End|(RICOH THETA V, Z1) <br/> "com.theta360.plugin.ACTION_AUDIO_SH_CLOSE"<br/><br/>(RICOH THETA X) <br/>"com.theta360.plugin.ACTION_AUDIO_SHUTTER_CLOSE" |
|Video Recording Start Audio|(RICOH THETA V, Z1) <br/> "com.theta360.plugin.ACTION_AUDIO_MOVSTART"<br/><br/>(RICOH THETA X) <br/>"com.theta360.plugin.ACTION_AUDIO_MOVIE_START" |
|Video Recording Stop Audio|(RICOH THETA V, Z1) <br/> "com.theta360.plugin.ACTION_AUDIO_MOVSTOP"<br/><br/>(RICOH THETA X) <br/>"com.theta360.plugin.ACTION_AUDIO_MOVIE_STOP" |
|Self Timer Audio|"com.theta360.plugin.ACTION_AUDIO_SELF"|
|Warning Audio|"com.theta360.plugin.ACTION_AUDIO_WARNING"|

When the THETA Plugin library is not used:
```
sendBroadcast(new Intent("com.theta360.plugin.ACTION_AUDIO_SHUTTER"));
```

When using the THETA Plugin library:

*Each Intent has its own method.
```
notificationAudioShutter();
```

## Control WLAN

Plugins can control WLAN. WLAN can be controlled by using Broadcast Intent corresponding to each WLAN operation mode.
If a developer registration AP restriction is applied, it is not possible to switch to CL Mode.  

|Operation Mode|Intent|
|:-|:-|
|OFF|"com.theta360.plugin.ACTION_WLAN_OFF"|
|AP Mode|"com.theta360.plugin.ACTION_WLAN_AP"|
|CL Mode|"com.theta360.plugin.ACTION_WLAN_CL"|

When the THETA Plugin library is not used:
```
sendBroadcast(new Intent("com.theta360.plugin.ACTION_WLAN_OFF"));
```

When using the THETA Plugin library:

*Each Intent has its own method.
```
notificationWlanOff();
```

## Control Bluetooth

Supported by THETA X Version 2.00.0 or later.  
Bluetooth can be turned on/off by following Broadcast Intent. 

|Operation Mode|Intent|
|:-|:-|
|OFF|"com.theta360.plugin.ACTION_BLUETOOTH_OFF"|
|ON |"com.theta360.plugin.ACTION_BLUETOOTH_ON"|

THETA Plugin library supports a method to send broadcast.

```
notificationBluetoothOff();
notificationBluetoothOn();
```

## Control GPS

Supported by THETA X Version 2.00.0 or later.  
GPS can be turned on/off by following Broadcast Intent. 

|Operation Mode|Intent|
|:-|:-|
|OFF|"com.theta360.plugin.ACTION_GPS_TAG_RECORDING_OFF"|
|ON |"com.theta360.plugin.ACTION_GPS_TAG_RECORDING_ON"|

THETA Plugin library supports a method to send broadcast.

```
notificationGpsOff();
notificationGpsOn();
```

## Control IMU Sensor

Supported by THETA V and Z1 only.  
IMU Sensor can be turned on/off by following Broadcast Intent.  
This is mandatory to execute zenith correction if plugin uses Camera API.

|Operation Mode|Intent|
|:-|:-|
|STOP|"com.theta360.plugin.ACTION_MOTION_SENSOR_STOP"|
|START |"com.theta360.plugin.ACTION_MOTION_SENSOR_START"|

THETA Plugin library supports a method to send broadcast.

```
notificationSensorStop();
notificationSensorStart();
```

## Control Battery Charging

Supported by THETA X firmware v2.20.1 or later.  
Battery charging can be suspended/resumed by following Broadcast Intent.  
Please note that THETA will power down soon after sending ACTION_BATTERY_CHARGING_RESUME when the battery level is almost 0%.

|Operation Mode|Intent|
|:-|:-|
|SUSPEND|"com.theta360.plugin.ACTION_BATTERY_CHARGING_SUSPEND"|
|RESUME |"com.theta360.plugin.ACTION_BATTERY_CHARGING_RESUME"|

THETA Plugin library supports a method to send broadcast.

```
notificationBatteryChargingSuspend();
notificationBatteryChargingResume();
```

## Updating the Database

RICOH THETA V, Z1 and X save image data in a database. When image data is moved or deleted, it is necessary to update the database so that inconsistencies does not occur in the database.

When using "com.theta360.plugin.ACTION_DATABASE_UPDATE" with Broadcast Intent, the database will be updated. When using Broadcast Intent, the following extension data must be set:

|Key|Type|Description|
|:-|:-|:-|
|targets|String Array|Directory path or file path array (RICOH THETA V, Z1)<br/>Example: ["DCIM/100RICOH/R0010001.JPG","DCIM/101RICOH"]|
|target|String Array|File path (RICOH THETA X)|

### RICOH THETA V / Z1  

With targets, specify the updated target file. If targets is not specified, Broadcast Intent is ignored. If you specify a directory, the files under that directory will be updated. Specify the path /sdcard/DCIM directory as below. It can be included even if the directory path or file path contains uppercase / lowercase letters.

When the THETA Plugin library is not used:
```
Intent intent = new Intent("com.theta360.plugin.ACTION_DATABASE_UPDATE");
intent.putExtra("targets", "DCIM/100RICOH/R0010001.JPG");
sendBroadcast(intent);
```
When using the THETA Plugin library:
```
notificationDatabaseUpdate("DCIM/100RICOH/R0010001.JPG");
```

### RICOH THETA X  

Only the full path can be specified for "target". Folders and multiple files cannot be specified. Additionally, folder names and file names must comply with DCF rules, and media must be in Equirectangular format and must not be 8K video (it must be suitable for playback in the camera UI). 
For internal memory, target = "storage/emulated/0/DCIM/100_TEST/R0000001.MP4"
For microSD cards, target = "storage/BSC8-1948/DCIM/100_TEST/R0000001.MP4"

When the THETA Plugin library is not used:
```
Intent intent = new Intent("com.theta360.plugin.ACTION_DATABASE_UPDATE");
intent.putExtra("target", "storage/emulated/0/DCIM/100_TEST/R0000001.MP4");
sendBroadcast(intent);
```
When using the THETA Plugin library:
```
notificationDatabaseUpdate("storage/emulated/0/DCIM/100_TEST/R0000001.MP4");
```

## Notifying Occurrences of Errors

When using "com.theta360.plugin.ACTION_ERROR_OCCURED" with Broadcast Intent, a notification that an error in the plugin has occurred will be sent. When receiving this notification, the camera plays a warning tone and blinks LED2 in red.

When the THETA Plugin library is not used:
```
sendBroadcast(new Intent("com.theta360.plugin.ACTION_ERROR_OCCURED"));
```
When using the THETA Plugin library:
```
notificationErrorOccured();
```

## Notifying Completion of Plugin

When using "com.theta360.plugin.ACTION_FINISH_PLUGIN" with Broadcast Intent, notification of the completion of the plugin will be sent. When using Broadcast Intent, the following extension data must be set:

|Key|Type|Description|
|:-|:-|:-|
|packageName|String|Package Name|
|exitStatus|String|"success" or "failure". Default is "success".|
|message|String|Optional. Default is an empty string.|

With packageName, specify the package name of the plugin itself. With exitStatus, specify "success" when the plugin ends normally, and "failure" when it ends abnormally. Setting "exitStatus" to "failure" will cause the warning sound to be played and LED2 to blink red.  
For the RICOH THETA X, this intent must be sent when the plugin is closed, but to close the plugin completely, it must be closed using onPause() or finish().

When the THETA Plugin library is not used:
```
Intent intent = new Intent("com.theta360.plugin.ACTION_FINISH_PLUGIN");
intent.putExtra("packageName", "The name of the package you are creating.");
intent.putExtra("exitStatus", "success");
sendBroadcast(intent);
```
When using the THETA Plugin library:
```
notificationSuccess();
```

## Notifying Camera Device Control

### RICOH THETA V / Z1  
When using "com.theta360.plugin.ACTION_MAIN_CAMERA_CLOSE" with Broadcast Intent, the fact that the plugin is controlling camera resources will be reported to the camera, and the [Camera API](camera-api.md) will be able to be used.

When the THETA Plugin library is not used:
```
sendBroadcast(new Intent("com.theta360.plugin.ACTION_MAIN_CAMERA_CLOSE"));
```
When using the THETA Plugin library:
```
notificationCameraClose();
```

When using "com.theta360.plugin.ACTION_MAIN_CAMERA_OPEN" with Broadcast Intent, the fact that the plugin has released camera resources will be reported to the camera, and the [Camera API](camera-api.md) will not be able to be used.

When the THETA Plugin library is not used:
```
sendBroadcast(new Intent("com.theta360.plugin.ACTION_MAIN_CAMERA_OPEN"));
```
When using the THETA Plugin library:
```
notificationCameraOpen();
```

### RICOH THETA X  
To shoot with the WebAPI, use "com.theta360.plugin.ACTION_PLUGIN_WEBAPI_CAMERA_OPEN".  

When the THETA Plugin library is not used:
```
sendBroadcast(new Intent("com.theta360.plugin.ACTION_PLUGIN_WEBAPI_CAMERA_OPEN"));
```
When using the THETA Plugin library:
```
notificationWebApiCameraOpen();
```

When finishing shooting with the WebAPI (closing the plugin), use "com.theta360.plugin.ACTION_PLUGIN_WEBAPI_CAMERA_CLOSE".

When the THETA Plugin library is not used:
```
sendBroadcast(new Intent("com.theta360.plugin.ACTION_PLUGIN_WEBAPI_CAMERA_CLOSE"));
```
When using the THETA Plugin library:
```
notificationWebApiCameraClose();
```
