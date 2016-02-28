CarOS 15.12 - Basketane
=======================

* security fixes from poky-upstream:
	* readline: CVE-2014-2524
	* openssh: CVE-2015-5600
	* unzip: CVE-2015-7696, CVE-2015-7697
	* libxslt: CVE-2015-7995

* basic support for host based firewall (native tools + rule persistence)

* preliminary support for self-hosted package feeds (added "kellner")

* added tools required for virtualization:
	* qemu
	* libvirtd
	* virsh
	* added openvswitch

* changed ext3-blocksize to 4k on lamobo sdcard-images
  (allows conversion to btrfs filesystem)

* updated golang-1.4.2 to 1.4.3

* added unbound and nsd packages for DNS resolving and zone-serving

* added nginx-1.9.6


CAROS 16.02
===========

Upgrade note (for building brands):

	* bitbake -c cleanall opkg opkg-native
	  opkg changed the way packages are checksummed
	* fixes from poky upstream:
	  * CVE-2016-0755 curl: NTLM credentials not-checked for proxy connection re-use
	  * CVE-2016-0754 curl: remote file name path traversal in curl tool for Windows
	  * socat: Security fix CVE-2016-2217
	  * nettle: Security fix CVE-2015-8803 and CVE-2015-8805
	  * CVE-2015-8370 grub2: buffer overflow when checking password entered during bootup
	  * libxml2: Security fix CVE-2015-8241
	  * pcre security fixes: CVE-2015-3210 CVE-2015-3217 CVE-2015-5073 CVE-2015-8388 CVE-2015-8380 CVE-2015-8381 CVE-2015-8383 CVE-2015-8384 CVE-2015-8385 CVE-2015-8386 CVE-2015-8387 CVE-2015-8389 CVE-2015-8390 CVE-2015-8392 CVE-2015-8393 CVE-2015-8394 CVE-2015-8395 CVE-2016-1283
	  * qemu: Security fix CVE-2015-7295
	  * qemu: Security fix CVE-2016-1568
	  * qemu: Security fix CVE-2015-8345
	  * qemu: Security fix CVE-2015-7512
	  * qemu: Security fix CVE-2015-7504
	  * qemu: Security fix CVE-2015-8504
	  * openssl: Security fix CVE-2016-0701
	  * openssl: Security fix CVE-2015-3197
	  * openssh: CVE-2016-1907
	  * glibc: CVE-2015-8776
	  * glibc: CVE-2015-9761
	  * glibc: CVE-2015-8779
	  * glibc: CVE-2015-8777
