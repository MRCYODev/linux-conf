# Pipewire conf

Make the folder
```
mkdir -p ~/.config/pipewire/pipewire.conf.d
```
---
Use nano or vim
```
nano ~/.config/pipewire/pipewire.conf.d/10-rate.conf
```

Config settings
```
context.properties = {  
   default.clock.rate = 96000  
   default.clock.allowed-rates = [ 44100 48000 88200 96000 ]  
}
```

Restart PipeWire services
```
systemctl --user restart pipewire pipewire-pulse wireplumber
```
---

# Elisa music player Fix
```
nano ~/.config/plasma-workspace/env/qt-audio-fix.sh
```
```
#!/bin/bash
export QT_AUDIO_BACKEND=pulseaudio
```
```
chmod +x ~/.config/plasma-workspace/env/qt-audio-fix.sh
```

