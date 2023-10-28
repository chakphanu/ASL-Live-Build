# ASL-Live-Build

ISO and IMG creator for the ASL 2.0.0 distribution using Debian live-build.

* Creates ISOs for net install for Intel/AMD64
* Creates IMG files for Raspberry Pi2, 3, and 4

## Requirements
You must install Debian Live before you can build. 

<pre>
sudo apt-get install qemu-user-static qemu-utils qemu-system-arm
sudo apt-get install build-essential live-build debootstrap apt-cacher-ng curl parted dosfstools zip xxd
</pre>

Consult this installation guide if you have other issues:

https://live-team.pages.debian.net/live-manual/html/live-manual/installation.en.html#118

## Building
For x86_86 live boot / installer
<pre>
make pc
</pre>

For Raspberry Pi 2, 3, 4 image
<pre>
make pi
</pre>

For Raspberry Pi4 must run in 32Bit mode(dahdi driver), add this to /boot/config.txt and reboot.
<pre>
arm_64bit=0
</pre>
## Contributors
Adam KC1KCC

Rob KK9ROB

Contributors to AllStarLink itself can be found here:
https://wiki.allstarlink.org/wiki/Credits_/_Contributions

## License

ASL-Live-Build is open-sourced software licensed under the GPLv3 License

(C) 2021 AllStarLinkInc
