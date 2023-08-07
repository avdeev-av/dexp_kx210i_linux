# Linux on DEXP Ursus KX210I

## Instructions
* Follow instructions on https://linuxiumcomau.blogspot.com/ to respin your linux distro. 
This gives more chances that live mode and installing will start properly and wifi, bluetooth and sound will work OOTB
* Clone this repo and insert files in their locations on your system
* Reboot
* `sudo apt-get install inotify-tools` to make rotate.sh work
* Try rotate.sh (then add to autostart)

## Debug
* Wrong screen rotations -> change actions in `/usr/share/autorotate/rotate.sh`
* Touchscreen issues after modifing rotate.sh -> swap (or change) coordinate transformation matrices

## Additions and References
* Tested on Mint 19.03 Xfce and 20.03 Xfce (With upgrades to 21, 21.1, 21.2)
* Kernels 5.15 and 6.2 works good. Boot using 5.19 failed
* Respin command:
`./isorespinner.sh -i mint.iso -b GRUB-32 -l rtl8723bt_4.12.0_amd64.deb -f linuxium-install-UCM-files.sh -f wrapper-linuxium-install-UCM-files.sh -f linuxium-install-broadcom-drivers.sh -f wrapper-linuxium-install-broadcom-drivers.sh -c wrapper-linuxium-install-UCM-files.sh -c wrapper-linuxium-install-broadcom-drivers.sh`

* https://linuxiumcomau.blogspot.com/
* https://github.com/znoxx/mint-tw52
* https://github.com/onitake/gsl-firmware
