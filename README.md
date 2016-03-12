# MLWG3

Kingston Mobilelite Wireless G3

#### Telnet
Create a file with the name 'mlwG3_v;telnetd; .x.x.bin' at the root level (USB-Stick ord SD-Card)
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
