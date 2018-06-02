# gentoo-kernel-config
My stable kernel configuration in Gentoo Linux

System:    Host: BlackHole Kernel: 4.14.47-gentoo-LTS-v0.0.1 x86_64 bits: 64 gcc: 6.4.0 Console: tty 3
           Distro: Gentoo Base System release 2.4.1
Machine:   Device: desktop Mobo: ASUSTeK model: B150M PRO GAMING v: Rev X.0x serial: 160470380401729
           UEFI: American Megatrends v: 0401 date: 01/18/2016
CPU:       Quad core Intel Core i5-6400 (-MCP-) arch: Skylake-S rev.3 cache: 6144 KB
           flags: (lm nx sse sse2 sse3 sse4_1 sse4_2 ssse3 vmx) bmips: 21696
           clock speeds: max: 3300 MHz 1: 2700 MHz 2: 2699 MHz 3: 2700 MHz 4: 2700 MHz
Graphics:  Card: NVIDIA GP107 [GeForce GTX 1050] bus-ID: 01:00.0
           Display Server: X.org 1.19.5 driver: nvidia tty size: 213x58 Advanced Data: N/A for root out of X
Audio:     Card-1 NVIDIA GP107GL High Definition Audio Controller driver: snd_hda_intel bus-ID: 01:00.1
           Card-2 Intel Sunrise Point-H HD Audio driver: snd_hda_intel bus-ID: 00:1f.3
           Sound: Advanced Linux Sound Architecture v: k4.14.47-gentoo-LTS-v0.0.1
Network:   Card: Intel Ethernet Connection (2) I219-V driver: e1000e bus-ID: 00:1f.6
           IF: enp0s31f6 state: up speed: 100 Mbps duplex: full mac: xx:xx:xx:xx:xx:xx
Drives:    HDD Total Size: 2240.5GB (2.4% used)
           ID-1: /dev/sda model: KINGSTON_SUV400S size: 120.0GB
           ID-2: /dev/sdb model: KINGSTON_SUV400S size: 120.0GB
           ID-3: /dev/sdc model: WDC_WD10EZEX size: 1000.2GB
           ID-4: /dev/sdd model: WDC_WD10EZEX size: 1000.2GB
Partition: ID-1: / size: 112G used: 4.7G (5%) fs: btrfs dev: /dev/mapper/gentoovg-root
           ID-2: /boot size: 238M used: 30M (14%) fs: ext4 dev: /dev/md125
           ID-3: /home size: 883G used: 41G (5%) fs: ext4 dev: /dev/dm-5
           ID-4: swap-1 size: 4.29GB used: 0.00GB (0%) fs: swap dev: /dev/dm-3
RAID:      Device-1: /dev/md125 - active components: online: sda2[0] sdb2[1]
           Info: raid: 1 report: 2/2 blocks: 255808 chunk size: N/A
           Device-2: /dev/md126 - active components: online: sda3[0] sdb3[1]
           Info: raid: 1 report: 2/2 blocks: 116693440 chunk size: N/A bitmap: true
           Device-3: /dev/md127 - active components: online: sdc1[0] sdd1[1]
           Info: raid: 1 report: 2/2 blocks: 976630464 chunk size: N/A bitmap: true
Sensors:   System Temperatures: cpu: 29.8C mobo: 27.8C gpu: 0.0:
           Fan Speeds (in rpm): cpu: N/A
Info:      Processes: 189 Uptime: 1:59 Memory: 2863.0/15962.3MB
           Init: SysVinit rc: OpenRC runlevel: default Gcc sys: 6.4.0 Client: Shell (zsh 5.5) inxi: 2.3.56


VERSIONS:
This current file correspond to my <b>working</b> setup using <b><i>Gentoo Linux</i></b>

REASONS:

<b>13:50/2018-06-02</b> -> <i>(Working)</i>, edid manual resolutions now available, switched to gentoo-sorces, boot over efi, disable nouveau (nvidia.ko is being loaded now), minor version changed, disable unused drivers, add support for btrfs

<b>21:29/2018-03-19</b> -> <i>(Working)</i>, still using last kernel commit, KVM (not guest) support added (read commit for info)

<b>10:48/2018-03-17</b> -> <i>(Working)</i>, gentoo-sources 4.4.87-r1 and 4.9.76-r1 still not recognizing my graphic card and generating random kernel panics when using ALSA without pulseaudio. Solution, copied oldconfig from 4.9.76-r1 and compiled it from official kernel.org using 4.14.27 sources.
https://git.kernel.org/pub/scm/linux/kernel/git/stable/linux-stable.git/log/?h=v4.14.27

<b>18:06/2018-03-16</b> -> <i>(Not working)</i> Trying latest stable version, now with same oldconfig from 4.9.76-r1 when adding ALSA support generates kernel panic at boot
https://gitweb.gentoo.org/repo/gentoo.git/tree/sys-kernel/gentoo-sources/gentoo-sources-4.15.10.ebuild

<b>21:19/2018-03-15</b> -> <i>(Not working)</i> Gentoo Linux still using Kernel version 4.9.76, but it was giving me some problems with Nouveau and non detected soundcard
https://gitweb.gentoo.org/repo/gentoo.git/tree/sys-kernel/gentoo-sources/gentoo-sources-4.9.76-r1.ebuil
