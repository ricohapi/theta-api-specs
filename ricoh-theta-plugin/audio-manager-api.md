# AudioManager API

In addition to the standard `android.media.AudioManager` API, RICOH THETA V and Z1 support the following custom parameters.
These parameters can be set using the `AudioManager.setParameters()` API.

## B-format Selection

To set B-format selection, set value for `"RicUseBFormat"`.
If you use microphone with Android standard APIs, call `setParameters("RicUseBFormat=false")` before using microphone.  

| Value | Description |
|:--|:--|
| `"true"`  | Ambisonics B-format (4ch) |
| `"false"` | Monaural (1ch) |

```java
AudioManager audioManager = (AudioManager) getSystemService(Context.AUDIO_SERVICE);
audioManager.setParameters("RicUseBFormat=true");
```

## Microphone Selection

To configure the microphone selection, set a value for `"RicMicSelect"`.  

| Value | Description |
|:--|:--|
| `"RicMicSelectAuto"`     | Auto |
| `"RicMicSelectInternal"` | Internal Mic |
| `"RicMicSelectExternal"` | External Mic<sup>\*1</sup> |

<sup>\*1</sup> RICOH THETA V only

```java
AudioManager audioManager = (AudioManager) getSystemService(Context.AUDIO_SERVICE);
mAudioManager.setParameters("RicMicSelect=RicMicSelectAuto");
```

## Microphone Gain

To set the microphone gain, set a value for `"RicMicSurroundVolumeLevel"`.  

| Value | Description |
|:--|:--|
| `"RicMicSurroundVolumeLevelNormal"` | Normal gain |
| `"RicMicSurroundVolumeLevelLarge"`  | Low gain for a loud environment |

```java
AudioManager audioManager = (AudioManager) getSystemService(Context.AUDIO_SERVICE);
mAudioManager.setParameters("RicMicSurroundVolumeLevel=RicMicSurroundVolumeLevelNormal");
```
