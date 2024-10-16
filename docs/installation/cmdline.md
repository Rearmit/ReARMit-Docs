!!! note
    Start from cli/server image from Armbian.

---
Login as user (not root) and execute the following commands


Add user to sudoers.
```bash
sudo echo "${USER} ALL=(ALL) NOPASSWD: ALL" >> /etc/sudoers
```

Update repo
```bash
sudo apt-get update
```

Install armbian-config
```bash
sudo apt-get -y install armbian-config
```

Install kernel headers
```bash
sudo /usr/sbin/armbian-config main=Software selection=Headers_install
```

Upgrade
```bash
sudo apt-get upgrade -y
```

Install alsa and pulseaudio
```bash
sudo apt-get -y install alsa-utils pulseaudio pamixer
```

Clone the RetroPie script
```bash
git clone https://github.com/Rearmit/RetroPie-Setup /home/pi/RetroPie-Setup -b armbian
```

Run RetroPie Setup
```bash
sudo /home/pi/RetroPie-Setup/retropi_setup.sh
```
