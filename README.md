# Allstar-Asterisk-Full
Allstar-Asterisk-Full DEB packages for amd64 architecture
* Debian 11

-----------------------------------------------------------

### What is included in the DEB package:

* binaries, modules, configs, sounds and updatenodelist

### What is NOT included in the DEB package:

* dahdi

-----------------------------------------------------------

### Changes/Fixes:

* Fix timing issues (app_rpt) [revised in Rev#7]
* Fix segfault "PBX may not have terminated properly ..." (app_rpt) [revised in Rev#7]
* Refactored and revamp the code (app_rpt)
* Add "phonesendlinks" - similar to hamvoip (app_rpt)
* Add keychunk filter - by JimZAH (app_rpt)
* Add voxhangtime - by davidgsd (chan_usbradio)
* Fix a race condition (chan_echolink)
* Add APRS - send stats to aprs.fi [ER-N0CALL | EL-N0CALL] (chan_echolink)
* Add message about your echolink node - similar to hamvoip (chan_echolink)
* Echolink nodes/conferences are shown in names - if available (chan_echolink) [revised in Rev#7]
* Fix echolink direction status (app_rpt)
* Improve new call lookup method with DB update [revised in Rev#7] (chan_echolink)
* Log messages received from an EchoLink client to the ASL log file (chan_echolink)
* Add an option to dump node linklist statistics (app_rpt)
* Critical changes and fixes have been made to the asterisk core (asterisk)
* Add linked list message check and attempt to reconnect as needed (app_rpt)

### Notes for Large Hub operation:
For fewer than 80 directly connected nodes, 1 CPU/vCPU is sufficient.
For 80 or more directly connected nodes, 2 or more CPUs/vCPUs are required.

### DISCLAIMER:
This software is provided "as-is" and for experimental purposes only, with no warranties or guarantees of any kind.

-----------------------------------------------------------

### How to install (Debian 11):

* Install the DVSwitch Repo

<pre>
wget http://dvswitch.org/buster
chmod +x buster
./buster
apt update
</pre>

* Install Linux Headers and DVSwitch dahdi package

<pre>
apt -y install linux-headers-$(uname -r)
apt -y install allstar-dahdi-linux-dkms allstar-dahdi-linux-tools
reboot
</pre>

* Install ASL Dependencies

For amd64
<pre>
apt -y install libasound2 libc6 libcomerr2 libcurl4 libgcc1 libgsm1 libidn11 libiksemel3 \
libncurses5 libnewt0.52 libogg0 libpopt0 libpri1.4 libspeex1 libstdc++6 libusb-0.1-4 \
libvorbis0a libvorbisenc2 libwrap0 zlib1g
</pre>

* Download and install the Allstar-Asterisk-Full DEB package

For amd64
<pre>
wget https://raw.githubusercontent.com/DU8BL/Allstar-Asterisk-Full/main/allstar-asterisk-full_1.02-20240207-7_amd64.deb
dpkg -i allstar-asterisk-full_1.02-20240207-7_amd64.deb
</pre>

-----------------------------------------------------------

### Copyright

Asterisk 1.4.23pre is copyright Digium (https://www.digium.com)

app_rpt and associated programs (app_rpt suite) are copyright Jim Dixon, WB6NIL; AllStarLink, Inc.; and contributors

DVSwitch repo and packages are copyright Steve Zingman, N4IRS; Michael Zingman, N4IRR; and contributors
