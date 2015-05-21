WebSounder - Audio
=========

Play sounds with html5 audio tag.

## Initialization ##
Import plugin: ws-audio.js.
```
var audio = new WSAudio();
audio.init({
  'sounds': {
    'track_alias': {
      'file': 'track_fileName',
      'type': 'ogg'
    },
    'soundA': {
      'file': 'A_fileName',
      'volume': 1,
      'preload': false
    },
    'soundB': {
      'file': 'B_fileName',
      'loop': false
    }
  },
  'path': 'path/',
  'volume': 0.7,
  'loop': true,
  'autoplay': true,
  'preload': true
});
```

## Usage ##

### Settings ###

 - path (General)
 - autoplay (General)
 - preload (General, Sound object)
 - volume (General, Sound object)
 - loop (General, Sound object)
 - type (General, Sound object)

### API ###
 - play
```
audio.play('soundA');
audio.play('soundA', 'ogg');
audio.play();   // play the last track
```
 - pause
```
audio.pause('soundA');
audio.pause();   // pause the last played track
```
 - pauseAll
 - stop
```
audio.stop('soundA');
audio.stop();   // stop the last played track
```
 - stopAll
 - toggleMuted
 - setSoundVolume
```
audio.setSoundVolume('sound_A', 0.5);
audio.setSoundVolume(0.5);   // change the last played track's volume to 0.5
```
 - setVolume

   This method will influence all tracks, including those tracks were changed by `setSoundVolume`.
 - status