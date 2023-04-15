# Pop!_OS 🌕

## Installation

* Download image at <https://pop.system76.com/>
* Flash image to disk using balenaEtcher - <https://www.balena.io/etcher/>
* Boot PC to disk and walk through OS installation

## Post-installation Setup

## Updates and Fixes

### No Wifi

Using ethernet connection run the following then reboot:

```bash
sudo apt update
sudo apt upgrade
sudo apt remove backport-iwlwifi-dkms ## remove old incompatible wifi driver
sudo apt remove broadcom-sta-dkms ## remove old incompatible wifi driver
sudo apt install bcmwl-kernel-source ## this is to fix wifi adapter issue
sudo apt distro-upgrade
```

### Nvidia driver issues

Symptom: attempting to run `sudo apt update && sudo apt upgrade` results in errors like `Errors were encountered when processing: nvidia-dkms-510
 nvidia-driver-510`

```bash
sudo apt-get remove "*nividia*"
sudo apt install pop-desktop system76-driver-nvidia
sudo apt autoremove --purge
sudo apt update -m
sudo dpkg --configure -a
sudo apt install -f
sudo reboot
```

## Customization

### Install gnome-extensions

```bash
sudo apt install chrome-gnome-shell
```

<https://extensions.gnome.org/>

### Install gnome-tweaks

```bash
sudo apt install gnome-tweaks
```

### Install ocs-url

<https://www.opendesktop.org/p/1136805/>

### Browse themes and cursors

<https://www.gnome-look.org/>

* Favorite theme - orchis gtk <https://www.gnome-look.org/p/1357889/>
* Favorite cursor pack - oreo cursors <https://www.gnome-look.org/p/1360254/>

### Install zsh and zsh-syntax-highlighting

<https://ohmyz.sh/#install>
<https://github.com/zsh-users/zsh-syntax-highlighting/blob/master/INSTALL.md#in-your-zshrc>
<https://draculatheme.com/zsh>
<https://draculatheme.com/zsh-syntax-highlighting>

### Brave Browser

```bash
sudo apt install curl

sudo curl -fsSLo /usr/share/keyrings/brave-browser-archive-keyring.gpg <https://brave-browser-apt-release.s3.brave.com/brave-browser-archive-keyring.gpg>

echo "deb [signed-by=/usr/share/keyrings/brave-browser-archive-keyring.gpg] <https://brave-browser-apt-release.s3.brave.com/> stable main"|sudo tee /etc/apt/sources.list.d/brave-browser-release.list

sudo apt update

sudo apt install brave-browser
```

## To Do

Find some dope icons! 🤘🤘🤘
