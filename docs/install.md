# RPM Fusion Installation
- [RPM](https://rpmfusion.org/)
- [Configuration](https://rpmfusion.org/Configuration)
- [Howto](https://rpmfusion.org/Howto)

## Free repository (Open source)
```cli
sudo dnf install -y \
  https://mirrors.rpmfusion.org/free/fedora/rpmfusion-free-release-$(rpm -E %fedora).noarch.rpm
```
## Nonfree repository (Closed source, NVIDIA drivers, some codecs)
```cli
sudo dnf install -y \
  https://mirrors.rpmfusion.org/nonfree/fedora/rpmfusion-nonfree-release-$(rpm -E %fedora).noarch.rpm
```
## Update everything.
```cli
sudo dnf group upgrade core -y
sudo dnf check-update
sudo dnf update -y
sudo reboot
```

# Firmware Updates

## See what can be updated.
```cli
sudo fwupdmgr get-devices
```

## Refresh the firmware database
```
sudo fwupdmgr refresh --force
```

## Check for updates
```cli
sudo fwupdmgr get-updates
```

## Apply them
```cli
sudo fwupdmgr update
sudo reboot
```

## PC Name
```cli
sudo hostnamectl set-hostname namehere
```

## Check here for anything else
[Fedora Linux Noble Setup](https://github.com/wz790/Fedora-Noble-Setup) - Useful Information

# Localsend Config
- [Localsend](https://localsend.org/download)
- Install localsend
```cli
flatpak install flathub org.localsend.localsend_app
flatpak run org.localsend.localsend_app
```
- Fix Localsend connection
- - check firewall status
```cli
sudo systemctl status firewalld
```
```cli
sudo firewall-cmd --permanent --add-port=53317/tcp
sudo firewall-cmd --permanent --add-port=53317/udp
sudo firewall-cmd --reload
```