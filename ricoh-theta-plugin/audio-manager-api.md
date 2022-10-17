# AudioManager API

In addition to android.media.AudioManager standard API, RICOH THETA V and Z1 support some specified parameters as listed below. These parameters can be set using AudioManager.setParameters API.

## B-format Selection
To set B-format selection, set value for "RicUseBFormat".
If you use microphone with Android standard APIs, call setParameters("RicUseBFormat=false") before using microphone.  

|Value|Description|
|:-|:-|
|"true"|Recording in Ambisonics B-format (4ch)|
|"false"|Recording in monaural (1ch)|

```
AudioManager audioManager = (AudioManager) getSystemService(Context.AUDIO_SERVICE);

audioManager.setParameters("RicUseBFormat=true");
```

## Microphone Selection
To set microphone selection, set value for "RicMicSelect".

|Value|Description|
|:-|:-|
|"RicMicSelectAuto"|Auto|
|"RicMicSelectInternal"|Internal Mic|
|"RicMicSelectExternal"|External Mic (RICOH THETA V only)|

```
AudioManager audioManager = (AudioManager) getSystemService(Context.AUDIO_SERVICE);

mAudioManager.setParameters("RicMicSelect=RicMicSelectAuto");
```

## Microphone Gain
To set microphone gain, set the value for "RicMicSurrondVolumeLevel".

|Value|Description|
|:-|:-|
|"RicMicSurroundVolumeLevelNormal"|Normal Mode|
|"RicMicSurroundVolumeLevelLarge"|Loud Mode (low gain)|

```
AudioManager audioManager = (AudioManager) getSystemService(Context.AUDIO_SERVICE);

mAudioManager.setParameters("RicMicSurroundVolumeLevel=RicMicSurroundVolumeLevelNormal");
```