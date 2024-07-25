# Allstar-Asterisk-Full
Allstar-Asterisk-Full DEB packages for amd64 architecture
* Debian 11 & 12

-----------------------------------------------------------

### What is included in the DEB package:

* dahdi, binaries, modules, configs, sounds and updatenodelist

-----------------------------------------------------------

### Notes:

* Use the current revision as much as possible to prevent known bugs from previous revisions.
* Address known bugs first before merging it into ASL3 base code.
* The Dahdi package is compatible for kernel version 6.X.

### Submitting Issues:

* Please submit any issues you encounter.

### Changes/Fixes:

* Includes most changes from Revision #8.
* Fixes a bug where app_rpt was not loading properly in Revision #8.
* Addresses high CPU utilization in app_rpt as the number of nodes increases.
* Adds AIOC to SimpleUSB and RadioUSB (no need to change PID and VID).
* Introduce additional options to the menu of simpleusb-tune-menu.

** HOTFIX **
* Fix the morse code issue from previous revisions.
* Fix a null dereference that leads to a SEGFAULT in app_rpt.

### Notes for Large Hub operation:

* For fewer than 90~100 directly connected nodes, 1 CPU/vCPU is sufficient.
* For 100 or more directly connected nodes, 2 or more CPUs/vCPUs is required (RECOMMENDED).

### DISCLAIMER:
This software is provided "as-is" and for experimental purposes only, with no warranties or guarantees of any kind.

-----------------------------------------------------------

### How to install (Debian 11 & 12):

* Update and Upgrade the system:

For Debian 11 & 12
<pre>
apt update
apt upgrade
reboot
</pre>

* Download and Install the Linux headers and DVSwitch DAHDI packages and dependencies:

For Debian 11 & 12
<pre>
wget https://raw.githubusercontent.com/DU8BL/Allstar-Asterisk-Full/main/allstar-dahdi-linux-dkms_3.1.0.20210216-19_all.deb
wget https://raw.githubusercontent.com/DU8BL/Allstar-Asterisk-Full/main/allstar-dahdi-linux-tools_3.1.0.20210205-4_amd64.deb
apt -y install linux-headers-$(uname -r)
apt -y install dkms libtonezone-dev fxload
dpkg -i allstar-dahdi-linux-dkms_3.1.0.20210216-19_all.deb
dpkg -i allstar-dahdi-linux-tools_3.1.0.20210205-4_amd64.deb
reboot
</pre>

* Install ASL Dependencies:

For Debian 11
<pre>
apt -y install libasound2 libc6 libcomerr2 libcurl4 libgcc1 libgsm1 libidn11 libiksemel3 \
libncurses5 libnewt0.52 libogg0 libpopt0 libpri1.4 libspeex1 libstdc++6 libusb-0.1-4 \
libvorbis0a libvorbisenc2 libwrap0 zlib1g
</pre>

For Debian 12
<pre>
apt -y install libasound2 libc6 libcom-err2 libcurl4 libgcc1 libgsm1 libidn11 libiksemel3 \
libncurses5 libnewt0.52 libogg0 libpopt0 libpri1.4 libspeex1 libstdc++6 libusb-0.1-4 \
libvorbis0a libvorbisenc2 libwrap0 zlib1g
</pre>

* Download and install the Allstar-Asterisk-Full package:

For Debian 11
<pre>
wget https://raw.githubusercontent.com/DU8BL/Allstar-Asterisk-Full/main/allstar-asterisk-full_1.02-20240723-9.1_deb11_amd64.deb
dpkg -i allstar-asterisk-full_1.02-20240723-9.1_deb11_amd64.deb
</pre>

For Debian 12
<pre>
wget https://raw.githubusercontent.com/DU8BL/Allstar-Asterisk-Full/main/allstar-asterisk-full_1.02-20240723-9.1_deb12_amd64.deb
dpkg -i allstar-asterisk-full_1.02-20240723-9.1_deb12_amd64.deb
</pre>

-----------------------------------------------------------

### Copyright

Asterisk 1.4.23pre is copyright Digium (https://www.digium.com)

app_rpt and associated programs (app_rpt suite) are copyright Jim Dixon, WB6NIL; AllStarLink, Inc.; and contributors

DVSwitch packages are copyright Steve Zingman, N4IRS; Michael Zingman, N4IRR; and contributors
