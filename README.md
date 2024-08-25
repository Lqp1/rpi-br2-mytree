# Custom Raspberrypi BuildRoot tree

## Summary

This config overrides `raspberrypi_defconfig` to tweak few things to my need:
- Rootfs is RO
- Admin's home is RW
- Default access is made using ssh (port 22), using admin/pass credentials
 
## Known limitations / bugs
- the gpio shutdown dtoverlay does not work
- ntpd does not start from the boot

## Futur work
