# FirmwareFS-toy
A free tool for working with the custom LittleFS images from Sigmastar.

For **usage and compilation** instructions, see the [original repository](https://github.com/tjko/littlefs-toy).

Based on lfs library from [OpenIPC SigmaStar Uboot](https://github.com/OpenIPC/u-boot-sigmastar/blob/6a5a2b67c1f54a5eb108c3809d474bb008fd1389/fs/firmwarefs/firmwarefs.c#L1).

Only tested for listing and extracting files, but creating new images should be possible as well.

Blocksize option is useless, as it is hardcoded to the [original firmwarefs implementation](https://github.com/OpenIPC/u-boot-sigmastar/blob/6a5a2b67c1f54a5eb108c3809d474bb008fd1389/fs/firmwarefs/firmwarefs.c#L269) with *CONFIG_MS_SPINAND* option, if your image was not built with this option you will need to change these values in `lfs_driver.c:238`.