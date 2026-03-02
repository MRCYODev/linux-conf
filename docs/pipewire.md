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

Config settings.
```
context.properties = {  
   default.clock.rate = 96000  
   default.clock.allowed-rates = [ 44100 48000 88200 96000 ]  
}
```

