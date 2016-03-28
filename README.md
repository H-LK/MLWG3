# MLWG3

Kingston Mobilelite Wireless G3

#### Telnet
Create a file with the name 'mlwG3_v;telnetd; .x.x.bin' at the root level (USB-Stick or SD-Card)
Plug it in and start the device.

Login as 'admin'

#### cat /proc/version
```
Linux version 2.6.36+ (terry_kuo@CVS2) (gcc version 4.6.3 (Buildroot 2012.11.1) ) #4 Fri Jan 8 09:03:01 CST 2016
```

#### cat /proc/cmdline
```
console=ttyS1,57600n8 root=/dev/ram0 console=
```

#### cat /proc/cpuinfo
```
system type             : MT7628
processor               : 0
cpu model               : MIPS 24Kc V5.5
BogoMIPS                : 386.04
wait instruction        : yes
microsecond timers      : yes
tlb_entries             : 32
extra interrupt vector  : yes
hardware watchpoint     : yes, count: 4, address/irw mask: [0x0000, 0x0778, 0x0c40, 0x0ee8]
ASEs implemented        : mips16 dsp
shadow register sets    : 1
core                    : 0
VCED exceptions         : not available
VCEI exceptions         : not available
```

#### cat /proc/filesystems
```
nodev   sysfs
nodev   rootfs
nodev   bdev
nodev   proc
nodev   tmpfs
nodev   sockfs
nodev   usbfs
nodev   pipefs
nodev   devpts
        ext2
        ext3
        ext4
nodev   ramfs
        vfat
        iso9660
nodev   jffs2
nodev   fuse
        fuseblk
nodev   fusectl
        udf
nodev   mtd_inodefs
        ufsd
```

#### cat /proc/mounts
```
rootfs / rootfs rw 0 0
proc /proc proc rw,relatime 0 0
none /var ramfs rw,relatime 0 0
none /dev ramfs rw,relatime 0 0
none /tmp ramfs rw,relatime 0 0
none /media ramfs rw,relatime 0 0
none /sys sysfs rw,relatime 0 0
none /proc/bus/usb usbfs rw,relatime 0 0
none /etc ramfs rw,relatime 0 0
mdev /dev ramfs rw,relatime 0 0
devpts /dev/pts devpts rw,relatime,mode=600 0 0
/dev/mtdblock5 /etc/config jffs2 rw,relatime 0 0
/dev/mmcblk0p1 /media/SD_Card1 vfat rw,relatime,fmask=0000,dmask=0000,allow_utime=0022,codepage=cp950,iocharset=utf8,shortname=mixed,errors=remount-ro 0 0
```

#### cat /proc/mtd
```
dev:    size   erasesize  name
mtd0: 00030000 00010000 "Bootloader"
mtd1: 00010000 00010000 "Config"
mtd2: 00010000 00010000 "Factory"
mtd3: 007b0000 00010000 "KernelA"
mtd4: 007b0000 00010000 "KernelB"
mtd5: 00050000 00010000 "User_CFG"
```
#### Serial port @ 57600
![alt tag](https://github.com/H-LK/MLWG3/blob/master/serial.jpg)

#### bootlog
```
�[05010C0B][05010C08]

DDR Calibration DQS reg = 0000888A



U-Boot 1.1.3 (Oct 22 2015 - 15:22:48)


Board: Ralink APSoC DRAM:  64 MB

relocate_code Pointer at: 83f68000

flash manufacture id: ef, device id 40 18

find flash: W25Q128BV

*** Check if data is correct or not...

*** Data is correct.

============================================

Ralink UBoot Version: 4.3.0.0

--------------------------------------------

ASIC 7628_MP (Port5<->None)

DRAM component: 512 Mbits DDR, width 16

DRAM bus: 16 bit

Total memory: 64 MBytes

Flash component: SPI Flash

Date:Oct 22 2015  Time:15:22:48

============================================

icache: sets:512, ways:4, linesz:32 ,total:65536

dcache: sets:256, ways:4, linesz:32 ,total:32768


 ##### The CPU freq = 575 MHZ ####

 estimate memory size =64 Mbytes

RESET MT7628 PHY!!!!!!

Please choose the operation:

   1: Load system code to SDRAM via TFTP.

   2: Load system code then write to Flash via TFTP.

   3: Boot system code via Flash (default).

   4: Entr boot command line interface.

   7: Load Boot Loader code then write to Flash via Serial.

   9: Load Boot Loader code then write to Flash via TFTP.



You choosed 3


 0



3: System Boot system code via Flash.

3: System Boot on bootstate=2.

## Booting image at bc800000 ...

   Image Name:   Linux Kernel Image

   Image Type:   MIPS Linux Kernel Image (lzma compressed)

   Data Size:    6161733 Bytes =  5.9 MB

   Load Address: 80000000

   Entry Point:  8000c150

   Verifying Checksum ... OK

   Uncompressing Kernel Image ... OK

No initrd

## Transferring control to Linux (at address 8000c150) ...

## Giving linux memsize in MB, 64


Starting kernel ...



LINUX started...

 THIS IS ASIC
Linux version 2.6.36+ (terry_kuo@CVS2) (gcc version 4.6.3 (Buildroot 2012.11.1) ) #4 Fri Jan 8 09:03:01 CST 2016

 The CPU feqenuce set to 575 MHz

 MIPS CPU sleep mode enabled.
CPU revision is: 00019655 (MIPS 24Kc)
Software DMA cache coherency
Determined physical RAM map:
 memory: 04000000 @ 00000000 (usable)
Initrd not found or empty - disabling initrd
Zone PFN ranges:
  Normal   0x00000000 -> 0x00004000
Movable zone start PFN for each node
early_node_map[1] active PFN ranges
    0: 0x00000000 -> 0x00004000
Built 1 zonelists in Zone order, mobility grouping on.  Total pages: 16256
Kernel command line: console=ttyS1,57600n8 root=/dev/ram0 console=
PID hash table entries: 256 (order: -2, 1024 bytes)
Dentry cache hash table entries: 8192 (order: 3, 32768 bytes)
Inode-cache hash table entries: 4096 (order: 2, 16384 bytes)
Primary instruction cache 64kB, VIPT, , 4-waylinesize 32 bytes.
Primary data cache 32kB, 4-way, PIPT, no aliases, linesize 32 bytes
Writing ErrCtl register=00051e2b
Readback ErrCtl register=00051e2b
Memory: 55104k/65536k available (4132k kernel code, 10388k reserved, 1136k data, 4296k init, 0k highmem)
NR_IRQS:128
console [ttyS1] enabled
Calibrating delay loop... 386.04 BogoMIPS (lpj=772096)
pid_max: default: 32768 minimum: 301
Mount-cache hash table entries: 512
NET: Registered protocol family 16
RALINK_GPIOMODE = 540d0404
RALINK_GPIOMODE = 540c0404
***** Xtal 40MHz *****
start PCIe register access
RALINK_RSTCTRL = 2400000
RALINK_CLKCFG1 = fdbfffc0

*************** MT7628 PCIe RC mode *************
PCIE0 enabled
Port 0 N_FTS = 1b105000
init_rt2880pci done
bio: create slab <bio-0> at 0
vgaarb: loaded
SCSI subsystem initialized
usbcore: registered new interface driver usbfs
usbcore: registered new interface driver hub
usbcore: registered new device driver usb
pci 0000:00:00.0: BAR 0: can't assign mem (size 0x80000000)
pci 0000:00:00.0: BAR 8: assigned [mem 0x20000000-0x201fffff]
pci 0000:00:00.0: BAR 1: assigned [mem 0x20200000-0x2020ffff]
pci 0000:00:00.0: BAR 1: set to [mem 0x20200000-0x2020ffff] (PCI address [0x20200000-0x2020ffff]
pci 0000:01:00.0: BAR 0: assigned [mem 0x20000000-0x200fffff]
pci 0000:01:00.0: BAR 0: set to [mem 0x20000000-0x200fffff] (PCI address [0x20000000-0x200fffff]
pci 0000:01:00.1: BAR 0: assigned [mem 0x20100000-0x201fffff]
pci 0000:01:00.1: BAR 0: set to [mem 0x20100000-0x201fffff] (PCI address [0x20100000-0x201fffff]
pci 0000:00:00.0: PCI bridge to [bus 01-01]
pci 0000:00:00.0:   bridge window [io  disabled]
pci 0000:00:00.0:   bridge window [mem 0x20000000-0x201fffff]
pci 0000:00:00.0:   bridge window [mem pref disabled]
BAR0 at slot 0 = 0
bus=0x0, slot = 0x0
res[0]->start = 0
res[0]->end = 0
res[1]->start = 20200000
res[1]->end = 2020ffff
res[2]->start = 0
res[2]->end = 0
res[3]->start = 0
res[3]->end = 0
res[4]->start = 0
res[4]->end = 0
res[5]->start = 0
res[5]->end = 0
bus=0x1, slot = 0x0
res[0]->start = 20000000
res[0]->end = 200fffff
res[1]->start = 0
res[1]->end = 0
res[2]->start = 0
res[2]->end = 0
res[3]->start = 0
res[3]->end = 0
res[4]->start = 0
res[4]->end = 0
res[5]->start = 0
res[5]->end = 0
bus=0x1, slot = 0x0
res[0]->start = 20100000
res[0]->end = 201fffff
res[1]->start = 0
res[1]->end = 0
res[2]->start = 0
res[2]->end = 0
res[3]->start = 0
res[3]->end = 0
res[4]->start = 0
res[4]->end = 0
res[5]->start = 0
res[5]->end = 0
Switching to clocksource Ralink Systick timer
NET: Registered protocol family 2
IP route cache hash table entries: 1024 (order: 0, 4096 bytes)
TCP established hash table entries: 2048 (order: 2, 16384 bytes)
TCP bind hash table entries: 2048 (order: 1, 8192 bytes)
TCP: Hash tables configured (established 2048 bind 2048)
TCP reno registered
UDP hash table entries: 256 (order: 0, 4096 bytes)
UDP-Lite hash table entries: 256 (order: 0, 4096 bytes)
NET: Registered protocol family 1
RT3xxx EHCI/OHCI init.
JFFS2 version 2.2 (NAND) (SUMMARY) (ZLIB) (RTIME) (CMODE_PRIORITY) (c) 2001-2006 Red Hat, Inc.
fuse init (API version 7.15)
msgmni has been set to 107
Block layer SCSI generic (bsg) driver version 0.4 loaded (major 254)
io scheduler noop registered (default)
Ralink gpio driver initialized
led=37, on=5, off=5, blinks,=4000, reset=1, time=4000
led=43, on=4000, off=1, blinks,=1, reset=1, time=4000
i2cdrv_major = 218
Serial: 8250/16550 driver, 2 ports, IRQ sharing enabled
serial8250: ttyS0 at MMIO 0x10000d00 (irq = 21) is a 16550A
serial8250: ttyS1 at MMIO 0x10000c00 (irq = 20) is a 16550A
brd: module loaded
flash0: started
flash manufacture id: ef, device id 40 18
W25Q128BV(ef 40180000) (16384 Kbytes)
mtd .name = raspi, .size = 0x01000000 (16M) .erasesize = 0x00010000 (64K) .numeraseregions = 0
Creating 6 MTD partitions on "raspi":
0x000000000000-0x000000030000 : "Bootloader"
0x000000030000-0x000000040000 : "Config"
0x000000040000-0x000000050000 : "Factory"
0x000000050000-0x000000800000 : "KernelA"
0x000000800000-0x000000fb0000 : "KernelB"
0x000000fb0000-0x000001000000 : "User_CFG"
rdm_major = 253
GMAC1_MAC_ADRH -- : 0x0000000c
GMAC1_MAC_ADRL -- : 0x43e17629
Ralink APSoC Ethernet Driver Initilization. v3.1  256 rx/tx descriptors allocated, mtu = 1500!
GMAC1_MAC_ADRH -- : 0x0000000c
GMAC1_MAC_ADRL -- : 0x43e17629
PROC INIT OK!
PPP generic driver version 2.4.2
PPP MPPE Compression module registered
NET: Registered protocol family 24
PPTP driver version 0.8.5


=== pAd = c01a5000, size = 1338600 ===

<-- RTMPAllocTxRxRingMemory, Status=0, ErrorValue=0x
<-- RTMPAllocAdapterBlock, Status=0
RtmpChipOpsHook(492): Not support for HIF_MT yet!
mt7628_init()-->
mt7628_init(FW(8a00), HW(8a01), CHIPID(7628))
e2.bin mt7628_init(1133)::(2), pChipCap->fw_len(63616)
mt_bcn_buf_init(218): Not support for HIF_MT yet!
<--mt7628_init()
ehci_hcd: USB 2.0 'Enhanced' Host Controller (EHCI) Driver
FM_OUT value: u4FmOut = 0(0x00000000)
FM_OUT value: u4FmOut = 140(0x0000008C)
FM detection done! loop = 1
SR calibration value u1SrCalVal = 6
rt3xxx-ehci rt3xxx-ehci: Ralink EHCI Host Controller
rt3xxx-ehci rt3xxx-ehci: new USB bus registered, assigned bus number 1
rt3xxx-ehci rt3xxx-ehci: irq 18, io mem 0x101c0000
rt3xxx-ehci rt3xxx-ehci: USB 0.0 started, EHCI 1.00
hub 1-0:1.0: USB hub found
hub 1-0:1.0: 1 port detected
ohci_hcd: USB 1.1 'Open' Host Controller (OHCI) Driver
rt3xxx-ohci rt3xxx-ohci: RT3xxx OHCI Controller
rt3xxx-ohci rt3xxx-ohci: new USB bus registered, assigned bus number 2
rt3xxx-ohci rt3xxx-ohci: irq 18, io mem 0x101c1000
hub 2-0:1.0: USB hub found
hub 2-0:1.0: 1 port detected
Initializing USB Mass Storage driver...
usbcore: registered new interface driver usb-storage
USB Mass Storage support registered.
usbcore: registered new interface driver usbserial
usbserial: USB Serial Driver core
USB Serial support registered for GSM modem (1-port)
usbcore: registered new interface driver option
option: v0.7.2:USB Driver for GSM modems
MTK MSDC device init.
mtk-sd: MediaTek MT6575 MSDC Driver
nf_conntrack version 0.5.0 (861 buckets, 3444 max)
IPVS: Registered protocols ()
IPVS: Connection hash table configured (size=4096, memory=32Kbytes)
IPVS: ipvs loaded.
GRE over IPv4 demultiplexor driver
gre: can't add protocol
ip_tables: (C) 2000-2006 Netfilter Core Team, Type=Restricted Cone
TCP cubic registered
NET: Registered protocol family 10
NET: Registered protocol family 17
L2TP core driver, V2.0
PPPoL2TP kernel driver, V2.0
802.1Q VLAN Support v1.8 Ben Greear <greearb@candelatech.com>
All bugs added by David S. Miller <davem@redhat.com>
msdc0 -> ops_get_cd return<0> <- msdc_ops_get_cd() : L<2319> PID<kworker/u:1><0x17>
Warning: unable to open an initial console.
Freeing unused kernel memory: 4296k freed
Algorithmics/MIPS FPU Emulator v1.5
ufsd: module license 'Commercial product' taints kernel.
Disabling lock debugging due to kernel taint
ufsd:: trace mask set to 0000000f
ufsd: driver (lke_8.9.0 lke_8.9.0_r225793_b93, LBD=ON, delalloc, ioctl, ugm, sd(1), wb, tr) loaded at c03d5000
NTFS support included
exFAT/TexFAT support included
optimized: speed
Build_for__Kingston_wifi_card_reader_k2.6.36_2013-03-22_lke_8.9.0_r225793_b93

ufsd: exfat can't store dates before Jan 1, 1980. Please update current date


=== pAd = c0882000, size = 1579488 ===

<-- RTMPAllocTxRxRingMemory, Status=0
<-- RTMPAllocAdapterBlock, Status=0
device_id =0x7650
==>MT76x0_WLAN_ChipOnOff(): OnOff:1, pAd->WlanFunCtrl:0x0, Reg-WlanFunCtrl=0xff000002
MACVersion = 0x76502000
led=11, on=1, off=4000, blinks,=1, reset=1, time=4000
led=7, on=1, off=4000, blinks,=1, reset=1, time=4000
led=43, on=4000, off=1, blinks,=1, reset=1, time=4000
Raeth v3.1 (Tasklet,SkbRecycle)

phy_tx_ring = 0x021e6000, tx_ring = 0xa21e6000

phy_rx_ring0 = 0x021e7000, rx_ring0 = 0xa21e7000
GMAC1_MAC_ADRH -- : 0x00000026
GMAC1_MAC_ADRL -- : (changed by HLK: MY MAC ADDRESS)
RT305x_ESW: Link Status Changed
device vlan0001 entered promiscuous mode
device eth2 entered promiscuous mode
br0: port 1(vlan0001) entering learning state
br0: port 1(vlan0001) entering learning state
init: can't log to /dev/tty5

starting pid 8441, tty '/dev/ttyS1': '/bin/sh'


BusyBox v1.12.1 (2016-01-08 08:19:59 CST) built-in shell (ash)
Enter 'help' for a list of built-in commands.

#
```
#### PCB
![alt tag](https://github.com/H-LK/MLWG3/blob/master/pcbtop.jpg)
![alt tag](https://github.com/H-LK/MLWG3/blob/master/pcbbottom.jpg)

#### swconfig
```
swconfig dev switch0 help
switch0: rt305x(rt305x-esw), ports: 7 (cpu @ 6), vlans: 4096
     --switch
	Attribute 1 (int): enable_vlan (VLAN mode (1:enabled))
	Attribute 2 (int): alternate_vlan_disable (Use en_vlan instead of doubletag to disable VLAN mode)
	Attribute 3 (int): bc_storm_protect (Global broadcast storm protection (0:Disable, 1:64 blocks, 2:96 blocks, 3:128 blocks))
	Attribute 4 (int): led_frequency (LED Flash frequency (0:30mS, 1:60mS, 2:240mS, 3:480mS))
	Attribute 5 (none): apply (Activate changes in the hardware)
	Attribute 6 (none): reset (Reset the switch)
     --vlan
	Attribute 1 (ports): ports (VLAN port mapping)
     --port
	Attribute 1 (int): disable (Port state (1:disabled))
	Attribute 2 (int): doubletag (Double tagging for incoming vlan packets (1:enabled))
	Attribute 3 (int): untag (Untag (1:strip outgoing vlan tag))
	Attribute 4 (int): led (LED mode (0:link, 1:100m, 2:duplex, 3:activity, 4:collision, 5:linkact, 6:duplcoll, 7:10mact, 8:100mact, 10:blink, 11:off, 12:on))
	Attribute 5 (int): lan (HW port group (0:wan, 1:lan))
	Attribute 6 (int): recv_bad (Receive bad packet counter)
	Attribute 7 (int): recv_good (Receive good packet counter)
	Attribute 8 (int): tr_bad (Transmit bad packet counter. rt5350 only)
	Attribute 9 (int): tr_good (Transmit good packet counter. rt5350 only)
	Attribute 10 (int): pvid (Primary VLAN ID)
	Attribute 11 (unknown): link (Get port link information)


```

### OpenWRT Buildroot Test
```

DDR Calibration DQS reg = 0000888A



U-Boot 1.1.3 (Oct 22 2015 - 15:22:48)


Board: Ralink APSoC DRAM:  64 MB

relocate_code Pointer at: 83f68000

flash manufacture id: ef, device id 40 18

find flash: W25Q128BV

*** Check if data is correct or not...

*** Data is correct.

============================================ 

Ralink UBoot Version: 4.3.0.0

-------------------------------------------- 

ASIC 7628_MP (Port5<->None)

DRAM component: 512 Mbits DDR, width 16

DRAM bus: 16 bit

Total memory: 64 MBytes

Flash component: SPI Flash

Date:Oct 22 2015  Time:15:22:48

============================================ 

icache: sets:512, ways:4, linesz:32 ,total:65536

dcache: sets:256, ways:4, linesz:32 ,total:32768 


 ##### The CPU freq = 575 MHZ #### 

 estimate memory size =64 Mbytes

RESET MT7628 PHY!!!!!!

Please choose the operation: 

   1: Load system code to SDRAM via TFTP. 

   2: Load system code then write to Flash via TFTP. 

   3: Boot system code via Flash (default).

   4: Entr boot command line interface.

   7: Load Boot Loader code then write to Flash via Serial. 

   9: Load Boot Loader code then write to Flash via TFTP. 

 0 

CFG_KERN_ADDR=bc050000   

3: System Boot system code via Flash.

3: System Boot on bootstate=0.

## Booting image at bc050000 ...

   Image Name:   MIPS OpenWrt Linux-4.4.6

   Image Type:   MIPS Linux Kernel Image (lzma compressed)

   Data Size:    1270134 Bytes =  1.2 MB

   Load Address: 80000000

   Entry Point:  80000000

   Verifying Checksum ... OK

   Uncompressing Kernel Image ... OK

No initrd

## Transferring control to Linux (at address 80000000) ...

## Giving linux memsize in MB, 64


Starting kernel ...


[    0.000000] Linux version 4.4.6 (hlk@Leno) (gcc version 5.3.0 (OpenWrt GCC 5.3.0 unknown) ) #3 Mon Mar 28 15:15:47 UTC 2016
[    0.000000] Board has DDR2
[    0.000000] Analog PMU set to hw control
[    0.000000] Digital PMU set to hw control
[    0.000000] SoC Type: MediaTek MT7628AN ver:1 eco:2
[    0.000000] bootconsole [early0] enabled
[    0.000000] CPU0 revision is: 00019655 (MIPS 24KEc)
[    0.000000] MIPS: machine is Kingston MLWG3
[    0.000000] Determined physical RAM map:
[    0.000000]  memory: 04000000 @ 00000000 (usable)
[    0.000000] Initrd not found or empty - disabling initrd
[    0.000000] Zone ranges:
[    0.000000]   Normal   [mem 0x0000000000000000-0x0000000003ffffff]
[    0.000000] Movable zone start for each node
[    0.000000] Early memory node ranges
[    0.000000]   node   0: [mem 0x0000000000000000-0x0000000003ffffff]
[    0.000000] Initmem setup node 0 [mem 0x0000000000000000-0x0000000003ffffff]
[    0.000000] Primary instruction cache 64kB, VIPT, 4-way, linesize 32 bytes.
[    0.000000] Primary data cache 32kB, 4-way, PIPT, no aliases, linesize 32 bytes
[    0.000000] Built 1 zonelists in Zone order, mobility grouping on.  Total pages: 16256
[    0.000000] Kernel command line: console=ttyS0,57600 rootfstype=squashfs,jffs2
[    0.000000] PID hash table entries: 256 (order: -2, 1024 bytes)
[    0.000000] Dentry cache hash table entries: 8192 (order: 3, 32768 bytes)
[    0.000000] Inode-cache hash table entries: 4096 (order: 2, 16384 bytes)
[    0.000000] Writing ErrCtl register=00016a2b
[    0.000000] Readback ErrCtl register=00016a2b
[    0.000000] Memory: 60844K/65536K available (2859K kernel code, 132K rwdata, 692K rodata, 148K init, 195K bss, 4692K reserved, 0K cma-reserved)
[    0.000000] SLUB: HWalign=32, Order=0-3, MinObjects=0, CPUs=1, Nodes=1
[    0.000000] NR_IRQS:256
[    0.000000] intc: using register map from devicetree
[    0.000000] CPU Clock: 580MHz
[    0.000000] clocksource_probe: no matching clocksources found
[    0.000000] clocksource: MIPS: mask: 0xffffffff max_cycles: 0xffffffff, max_idle_ns: 6590553264 ns
[    0.000011] sched_clock: 32 bits at 290MHz, resolution 3ns, wraps every 7405115902ns
[    0.015351] Calibrating delay loop... 385.84 BogoMIPS (lpj=1929216)
[    0.080520] pid_max: default: 32768 minimum: 301
[    0.089782] Mount-cache hash table entries: 1024 (order: 0, 4096 bytes)
[    0.102733] Mountpoint-cache hash table entries: 1024 (order: 0, 4096 bytes)
[    0.122183] clocksource: jiffies: mask: 0xffffffff max_cycles: 0xffffffff, max_idle_ns: 19112604462750000 ns
[    0.141681] pinctrl core: initialized pinctrl subsystem
[    0.152617] NET: Registered protocol family 16
[    0.164857] rt2880-pinmux pinctrl: invalid group "wled" for function "gpio"
[    0.192073] mt7621_gpio 10000600.gpio: registering 32 gpios
[    0.203159] mt7621_gpio 10000600.gpio: registering 32 gpios
[    0.214177] mt7621_gpio 10000600.gpio: registering 32 gpios
[    0.226689] clocksource: Switched to clocksource MIPS
[    0.238092] NET: Registered protocol family 2
[    0.247504] TCP established hash table entries: 1024 (order: 0, 4096 bytes)
[    0.261209] TCP bind hash table entries: 1024 (order: 0, 4096 bytes)
[    0.273722] TCP: Hash tables configured (established 1024 bind 1024)
[    0.286369] UDP hash table entries: 256 (order: 0, 4096 bytes)
[    0.297825] UDP-Lite hash table entries: 256 (order: 0, 4096 bytes)
[    0.310467] NET: Registered protocol family 1
[    0.320369] futex hash table entries: 256 (order: -1, 3072 bytes)
[    0.351065] squashfs: version 4.0 (2009/01/31) Phillip Lougher
[    0.362534] jffs2: version 2.2 (NAND) (SUMMARY) (LZMA) (RTIME) (CMODE_PRIORITY) (c) 2001-2006 Red Hat, Inc.
[    0.384547] io scheduler noop registered
[    0.392228] io scheduler deadline registered (default)
[    0.403217] Serial: 8250/16550 driver, 2 ports, IRQ sharing disabled
[    0.416616] rt2880-pinmux pinctrl: function 'uart0' not supported
[    0.428574] rt2880-pinmux pinctrl: invalid function uart0 in map table
[    0.441680] console [ttyS0] disabled
[    0.448669] 10000c00.uartlite: ttyS0 at MMIO 0x10000c00 (irq = 28, base_baud = 2500000) is a 16550A
[    0.466521] console [ttyS0] enabled
[    0.466521] console [ttyS0] enabled
[    0.480256] bootconsole [early0] disabled
[    0.480256] bootconsole [early0] disabled
[    0.497695] spi-mt7621 10000b00.spi: sys_freq: 193333333
[    0.511818] m25p80 spi32766.0: using chunked io (size=32)
[    0.522580] m25p80 spi32766.0: w25q128 (16384 Kbytes)
[    0.532623] 5 ofpart partitions found on MTD device spi32766.0
[    0.544180] Creating 5 MTD partitions on "spi32766.0":
[    0.554362] 0x000000000000-0x000000030000 : "u-boot"
[    0.565960] 0x000000030000-0x000000040000 : "u-boot-env"
[    0.578361] 0x000000040000-0x000000050000 : "factory"
[    0.590223] 0x000000050000-0x000000fb0000 : "firmware"
[    0.651220] 2 uimage-fw partitions found on MTD device firmware
[    0.662975] 0x000000050000-0x0000001861b6 : "kernel"
[    0.674440] 0x0000001861b6-0x000000fb0000 : "rootfs"
[    0.686128] mtd: device 5 (rootfs) set to be root filesystem
[    0.697496] 1 squashfs-split partitions found on MTD device rootfs
[    0.709749] 0x000000400000-0x000000fb0000 : "rootfs_data"
[    0.722303] 0x000000fb0000-0x000001000000 : "user-config"
[    0.744207] rt3050-esw 10110000.esw: link changed 0x00
[    0.755814] mtk_soc_eth 10100000.ethernet: generated random MAC address ea:a1:57:33:f7:41
[    0.772884] mtk_soc_eth 10100000.ethernet eth0: mediatek frame engine at 0xb0100000, irq 5
[    0.789816] mt7621_wdt 10000120.watchdog: Initialized
[    0.801417] NET: Registered protocol family 10
[    0.813827] NET: Registered protocol family 17
[    0.822787] bridge: automatic filtering via arp/ip/ip6tables has been deprecated. Update your scripts to load br_netfilter if you need this.
[    0.847796] 8021q: 802.1Q VLAN Support v1.8
[    0.867433] VFS: Mounted root (squashfs filesystem) readonly on device 31:5.
[    0.882224] Freeing unused kernel memory: 148K (8039b000 - 803c0000)
[    2.726091] init: Console is alive
[    2.733125] init: - watchdog -
[    4.575725] usbcore: registered new interface driver usbfs
[    4.586767] usbcore: registered new interface driver hub
[    4.597410] usbcore: registered new device driver usb
[    4.619084] SCSI subsystem initialized
[    4.633128] ehci_hcd: USB 2.0 'Enhanced' Host Controller (EHCI) Driver
[    4.647728] ehci-platform: EHCI generic platform driver
[    4.668397] phy phy-10120000.usbphy.0: remote usb device wakeup disabled
[    4.681678] phy phy-10120000.usbphy.0: UTMI 16bit 30MHz
[    4.692060] ehci-platform 101c0000.ehci: EHCI Host Controller
[    4.703480] ehci-platform 101c0000.ehci: new USB bus registered, assigned bus number 1
[    4.719290] ehci-platform 101c0000.ehci: irq 26, io mem 0x101c0000
[    4.746713] ehci-platform 101c0000.ehci: USB 2.0 started, EHCI 1.00
[    4.760267] hub 1-0:1.0: USB hub found
[    4.768100] hub 1-0:1.0: 1 port detected
[    4.779143] ohci_hcd: USB 1.1 'Open' Host Controller (OHCI) Driver
[    4.792919] ohci-platform: OHCI generic platform driver
[    4.803591] ohci-platform 101c1000.ohci: Generic Platform OHCI controller
[    4.817102] ohci-platform 101c1000.ohci: new USB bus registered, assigned bus number 2
[    4.832873] ohci-platform 101c1000.ohci: irq 26, io mem 0x101c1000
[    4.901816] hub 2-0:1.0: USB hub found
[    4.909689] hub 2-0:1.0: 1 port detected
[    4.929661] MTK MSDC device init.
[    4.936419] mtk-sd: MediaTek MT6575 MSDC Driver
[    4.947837] sdhci: Secure Digital Host Controller Interface driver
[    4.960119] sdhci: Copyright(c) Pierre Ossman
[    4.970056] sdhci-pltfm: SDHCI platform and OF driver helper
[    4.985650] usbcore: registered new interface driver usb-storage
[    5.008133] init: - preinit -
[    5.888255] rt3050-esw 10110000.esw: link changed 0x00
[    6.084910] random: procd urandom read with 9 bits of entropy available
Press the [f] key and hit [enter] to enter failsafe mode
Press the [1], [2], [3] or [4] key and hit [enter] to select the debug level
[    9.338334] mount_root: loading kmods from internal overlay
[   10.113178] jffs2: notice: (355) jffs2_build_xattr_subsystem: complete building xattr subsystem, 0 of xdatum (0 unchecked, 0 orphan) and 0 of xref (0 dead, 0 orphan) found.
[   10.144333] block: attempting to load /tmp/jffs_cfg/upper/etc/config/fstab
[   10.165347] block: extroot: not configured
[   10.309471] jffs2: notice: (352) jffs2_build_xattr_subsystem: complete building xattr subsystem, 0 of xdatum (0 unchecked, 0 orphan) and 0 of xref (0 dead, 0 orphan) found.
[   10.801825] block: attempting to load /tmp/jffs_cfg/upper/etc/config/fstab
[   10.821716] block: extroot: not configured
[   10.830929] mount_root: switching to jffs2 overlay
[   10.869742] procd: - early -
[   10.875558] procd: - watchdog -
[   11.680999] procd: - ubus -
[   11.740217] procd: - init -
Please press Enter to activate this console.
[   12.649639] ip6_tables: (C) 2000-2006 Netfilter Core Team
[   12.673794] Loading modules backported from Linux version v4.4-rc5-1913-gc8fdf68
[   12.688512] Backport generated by backports.git backports-20151218-0-g2f58d9d
[   12.756536] mt76_wmac 10300000.wmac: ASIC revision: 76280001
[   14.808546] mt76_wmac 10300000.wmac: Firmware Version: _e2_mp
[   14.819991] mt76_wmac 10300000.wmac: Build Time: 20150211175503
[   14.846691] firmware init done
[   15.042956] ip_tables: (C) 2000-2006 Netfilter Core Team
[   15.081100] nf_conntrack version 0.5.0 (953 buckets, 3812 max)
[   15.149312] usbcore: registered new interface driver ums-alauda
[   15.163488] usbcore: registered new interface driver ums-cypress
[   15.177947] usbcore: registered new interface driver ums-datafab
[   15.192170] usbcore: registered new interface driver ums-freecom
[   15.206551] usbcore: registered new interface driver ums-isd200
[   15.220828] usbcore: registered new interface driver ums-jumpshot
[   15.235247] usbcore: registered new interface driver ums-karma
[   15.249817] usbcore: registered new interface driver ums-sddr09
[   15.264045] usbcore: registered new interface driver ums-sddr55
[   15.278568] usbcore: registered new interface driver ums-usbat
[   15.312050] xt_time: kernel timezone is -0000
[   15.334806] PPP generic driver version 2.4.2
[   15.346421] NET: Registered protocol family 24
[   23.440924] IPv6: ADDRCONF(NETDEV_UP): br-lan: link is not ready
[   26.438265] IPv6: ADDRCONF(NETDEV_UP): wlan0: link is not ready
[   26.454713] device wlan0 entered promiscuous mode
[   26.980352] IPv6: ADDRCONF(NETDEV_CHANGE): wlan0: link becomes ready
[   26.993147] br-lan: port 1(wlan0) entered forwarding state
[   27.004079] br-lan: port 1(wlan0) entered forwarding state
[   27.021384] IPv6: ADDRCONF(NETDEV_CHANGE): br-lan: link becomes ready
[   28.996743] br-lan: port 1(wlan0) entered forwarding state
```
