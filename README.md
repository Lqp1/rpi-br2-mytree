# Custom Raspberrypi BuildRoot tree

## Summary

This config overrides `raspberrypi_defconfig` to tweak few things to my need:
- Rootfs is RO
- Admin's home is RW
- Default access is made using ssh (port 22), using admin/pass credentials

## Setup

```bash
$ git clone https://github.com/Lqp1/rpi-br2-mytree mytree
$ tar -xf buildroot-2024.02.5.tar.gz
$ cd buildroot-2024.02.5/
$ export BR2_EXTERNAL=../mytree
$ make myrasp_defconfig
$ make
```
Then flash the output `sdcard.img`
 
## Known limitations / bugs
- the gpio shutdown dtoverlay does not work
- ntpd does not start from the boot

## Future work
