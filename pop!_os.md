# Pop!_OS Installation 
* Download image at https://pop.system76.com/
* Flash image to disk using balenaEtcher - https://www.balena.io/etcher/
* Boot PC to disk and walk through OS installation

# Post-installation Setup
## Updates and Fixes
Using ethernet connection run the following then reboot:

    $ sudo apt update
    $ sudo apt upgrade
    $ sudo apt remove backport-iwlwifi-dkms ## remove old incompatible wifi driver
    $ sudo apt remove broadcom-sta-dkms ## remove old incompatible wifi driver
    $ sudo apt install bcmwl-kernel-source ## this is to fix wifi adapter issue
    $ sudo apt distro-upgrade
    
## Customization
### Install gnome-extensions:

    $ sudo apt install chrome-gnome-shell
https://extensions.gnome.org/

### Install gnome-tweaks:

    $ sudo apt install gnome-tweaks
    
### Install ocs-url
https://www.opendesktop.org/p/1136805/

### Browse themes and cursors
https://www.gnome-look.org/
* Favorite theme - orchis gtk https://www.gnome-look.org/p/1357889/
* Favorite cursor pack - oreo cursors https://www.gnome-look.org/p/1360254/

## To Do
Find some dope icons! 🤘🤘🤘
