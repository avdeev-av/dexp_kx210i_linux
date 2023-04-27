# Linux on DEXP Ursus KX210I

## Instructions
* Follow instructions on https://linuxiumcomau.blogspot.com/ to respin your linux distro. 
This gives more chances that live mode and installing will start properly and wifi, bluetooth and sound will work OOTB
* Clone this repo and insert files in their locations on your system
* Reboot
* sudo apt-get install inotify-tools` to make rotate.sh work
* Try `sudo /usr/share/autorotate/rotate.sh` (then add this script to autostart)
* To make sure touchscreen works fine, use `xinput_calibratior` and modify `usr/share/X11/xorg.conf.d/99-calibration.conf`

## Debug
* Wrong screen rotations -> change actions in `/usr/share/autorotate/rotate.sh`
* Touchscreen issues after modifing `rotate.sh` -> swap (or change) coordinate transformation matrices

## Additions and References
* Tested on Mint 19.03 Xfce (Upgraded to 20.03 Xfce), respin command:
`./isorespinner.sh -i mint.iso -b GRUB-32 -l rtl8723bt_4.12.0_amd64.deb -f linuxium-install-UCM-files.sh -f wrapper-linuxium-install-UCM-files.sh -f linuxium-install-broadcom-drivers.sh -f wrapper-linuxium-install-broadcom-drivers.sh -c wrapper-linuxium-install-UCM-files.sh -c wrapper-linuxium-install-broadcom-drivers.sh`

* https://linuxiumcomau.blogspot.com/
* https://github.com/znoxx/mint-tw52
* https://github.com/onitake/gsl-firmware
