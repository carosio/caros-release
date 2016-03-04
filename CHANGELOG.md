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

CAROS 16.02.2
=============

Updates from poky-upstream:

  * Corrected Note for CentOS package requirements
  * ref-manual: Updated the S variable description with feedback
  * ref-manual: Updated the staging.bbclass description
  * ref-manual: Updated the S variable description.
  * dev-manual, ref-manual: Updated licensing text information.
  * ref-manual: Added order information for conf file parsing.
  * openssl: Security fix CVE-2016-0800
  * wpa-supplicant: Fix CVE-2015-8041
  * build-appliance-image: Update to jethro head revision
  * qemu: Security fix CVE-2016-2198
  * qemu: Security fix CVE-2016-2197
  * libgcrypt: Security fix CVE-2015-7511
  * uclibc: Security fix CVE-2016-2225
  * uclibc: Security fix CVE-2016-2224
  * libbsd: Security fix CVE-2016-2090
  * glibc: Security fix CVE-2015-7547

Updates from meta-caros:

 * [erlang-gen-socket] update -> v0.5
 * [erlang-gen-netlink] update -> v1.2
 * [erlang-lager] update 2.1.1 -> 3.0.1
 * [erlang-goldrush] update 0.1.6 -> 0.1.7
 * upgrade flower to 0.3.7 for R18 compatibility
 * [erlang-dhcp] add initial recipe
 * [erlang] patch: support IPv6 node registration
 * [dropbear] no longer bbappend
 * [smartcapwap] patch: add verbosity
 * [smartcapwap] add initial recipe
 * [linux-caros] patch: allow 802.11 frame injection
 * [wolfssl] bbappend: configure crypto features
 * [linux-ptp] add linux-ptp (high precision time keeping) support
 * [bird] use official release tar-ball, fix cksums
 * bump hello -> 3.2.0
 * add hello dependency coverall
 * add erlang-cartifi 0.3.0
 * add erlang-mimerl 1.0.2
 * bump erlang-yang -> 2.2.2
 * add erlang-ssl-verify-hostname 1.0.5
 * add erlang-setup 1.5.0
 * add erlang-msgpack 0.3.4
 * bump erlang-jsx -> 2.6.2
 * add idna 1.0.3
 * add hackney 1.3.2
 * bump gen_listener_tcp -> 0.3.2
 * bump erlang folsom -> 0.8.2
 * enable erlang-meck 0.8.4
 * add erlang-parse-trans 2.9.2
 * update erlang-ranch -> 1.2.1
 * bump cowlib -> 1.0.2
 * bump erlang-cowboy -> 1.0.4
 * update erlang-goldrush 0.1.6
 * add hello dependency ezmq 1.0.0
 * bump ex_uri: 1.0.1r1 -> 1.0.1r2
 * bump erlang-lager: 2.1.0 -> 2.1.1
 * bump abnfc -> 0.3.1
 * bump bear: 0.1.4 -> 0.8.2
 * add hello dependency exometer_core 1.4.1
 * add hello dependecy edown 0.7.1
 * add hello dependency dnssd 0.9.0
 * reworked rebar class
 * bump: rebar 2.5.0-> 2.6.1
 * add recipe for smem 1.5
 * [libmnl] bump to libmnl-1.0.3-35-g1891e0e
