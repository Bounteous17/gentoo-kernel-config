# gentoo-kernel-config
My stable kernel configuration in Gentoo Linux

00:00.0 Host bridge: Intel Corporation Xeon E3-1200 v5/E3-1500 v5/6th Gen Core Processor Host Bridge/DRAM Registers (rev 07)
00:01.0 PCI bridge: Intel Corporation Xeon E3-1200 v5/E3-1500 v5/6th Gen Core Processor PCIe Controller (x16) (rev 07)
00:14.0 USB controller: Intel Corporation Sunrise Point-H USB 3.0 xHCI Controller (rev 31)
00:16.0 Communication controller: Intel Corporation Sunrise Point-H CSME HECI #1 (rev 31)
00:17.0 SATA controller: Intel Corporation Sunrise Point-H SATA controller [AHCI mode] (rev 31)
00:1c.0 PCI bridge: Intel Corporation Sunrise Point-H PCI Express Root Port #5 (rev f1)
00:1c.6 PCI bridge: Intel Corporation Sunrise Point-H PCI Express Root Port #7 (rev f1)
00:1d.0 PCI bridge: Intel Corporation Sunrise Point-H PCI Express Root Port #9 (rev f1)
00:1f.0 ISA bridge: Intel Corporation Sunrise Point-H LPC Controller (rev 31)
00:1f.2 Memory controller: Intel Corporation Sunrise Point-H PMC (rev 31)
00:1f.3 Audio device: Intel Corporation Sunrise Point-H HD Audio (rev 31)
00:1f.4 SMBus: Intel Corporation Sunrise Point-H SMBus (rev 31)
00:1f.6 Ethernet controller: Intel Corporation Ethernet Connection (2) I219-V (rev 31)
01:00.0 VGA compatible controller: NVIDIA Corporation GP107 [GeForce GTX 1050] (rev a1)
01:00.1 Audio device: NVIDIA Corporation GP107GL High Definition Audio Controller (rev a1)

VERSIONS:
This current file correspond to my <b>working</b> setup using <b><i>Gentoo Linux</i></b>

REASONS:

<b>10:48/2018-03-17</b> -> <i>(Working)</i>, gentoo-sources 4.4.87-r1 and 4.9.76-r1 still not recognizing my graphic card and generating random kernel panics when using ALSA without pulseaudio. Solution, copied oldconfig from 4.9.76-r1 and compiled it from official kernel.org using 4.14.27 sources.
https://git.kernel.org/pub/scm/linux/kernel/git/stable/linux-stable.git/log/?h=v4.14.27

<b>18:06/2018-03-16</b> -> <i>(Not working)</i> Trying latest stable version, now with same oldconfig from 4.9.76-r1 when adding ALSA support generates kernel panic at boot
https://gitweb.gentoo.org/repo/gentoo.git/tree/sys-kernel/gentoo-sources/gentoo-sources-4.15.10.ebuild

<b>21:19/2018-03-15</b> -> <i>(Not working)</i> Gentoo Linux still using Kernel version 4.9.76, but it was giving me some problems with Nouveau and non detected soundcard
https://gitweb.gentoo.org/repo/gentoo.git/tree/sys-kernel/gentoo-sources/gentoo-sources-4.9.76-r1.ebuil
