# Allstar-Asterisk-Full
Allstar-Asterisk-Full DEB package for the amd64 architecture

-----------------------------------------------------------

### What is included in the DEB package:

* binaries, modules, configs, sounds and updatenodelist

### What is NOT included in the DEB package:

* dahdi

-----------------------------------------------------------

### What is also Added:

* Some changes from ASL 2.0.0 distribution

-----------------------------------------------------------

### How to install (Debian):

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

<pre>
apt -y install libasound2 libc6 libcomerr2 libcurl4 libgcc1 libgsm1 libidn11 libiksemel3 \
libncurses5 libnewt0.52 libogg0 libpopt0 libpri1.4 libspeex1 libstdc++6 libvorbis0a \
libvorbisenc2 libwrap0 zlib1g
</pre>

* Download and install the Allstar-Asterisk-Full DEB package

<pre>
wget https://raw.githubusercontent.com/DU8BL/Allstar-Asterisk-Full/main/allstar-asterisk-full_1.02-20230206-3_amd64.deb
dpkg -i allstar-asterisk-full_1.02-20230206-3_amd64.deb
</pre>

-----------------------------------------------------------

### How to update (Debian):

* This will overwrite existing /etc/asterisk/ files. Be sure to backup the needed files before executing the commands.

<pre>
wget https://raw.githubusercontent.com/DU8BL/Allstar-Asterisk-Full/main/allstar-asterisk-full_1.02-20230206-3_amd64.deb
dpkg -i allstar-asterisk-full_1.02-20230206-3_amd64.deb
</pre>

-----------------------------------------------------------

Codebase from https://github.com/pttlink/Asterisk and https://github.com/AllStarLink/ASL-Asterisk

### Copyright

Asterisk 1.4.23pre is copyright Digium (https://www.digium.com)

app_rpt and associated programs (app_rpt suite) are copyright Jim Dixon, WB6NIL; AllStarLink, Inc.; and contributors

DVSwitch repo and packages are copyright Steve Zingman, N4IRS; Michael Zingman, N4IRR; and contributors
