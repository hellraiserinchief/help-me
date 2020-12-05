### Burning image
lsbls  
xz -d < console.img.xz - | dd of=/dev/mmcblk0p3


### BeagleBone
1. [Dekek Molly's Blog](http://derekmolloy.ie/beaglebone)
1. [Serial Connection](https://elinux.org/Beagleboard:BeagleBone_Black_Serial). 
1. Use minicom. 'minicom -D /dev/ttyUSB0'. Exit Alt-A then X. [ set harddware flow off in serial port settings to communication 2 way with BBB ]

https://www.reddit.com/r/BeagleBone/comments/2n3zji/cant_flash_emmc_with_sd_card/

### PocketBeagle
1. [System Reference Manual](https://github.com/beagleboard/pocketbeagle/wiki/System-Reference-Manual)
1. [Kin Shirriff's Blog](http://www.righto.com/2017/12/hands-on-with-pocketbeagle-tiny-25.html)

### Share internet using USB
https://gist.github.com/pdp7/d2711b5ff1fbb000240bd8337b859412
