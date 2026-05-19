see filelist.ini for the list of files found/to place here

required for each build type that will be supported by the files:
_retail.ini  : for retail images
_jtag.ini    : for jtag images
_glitch.ini  : for gg images
_glitch2.ini : for gg images using dual CB
_glitch3.ini : for gg images using triple CB
_devkit.ini  : for devkit images
_devgl.ini   : for devkit gg images
_rgbuild.ini : for RGLoader devkit conversion images

_jtag_bigflash.ini : alternate name used with -i bigflash option on command line
_jtag_xell.ini : alternate name used to replace CF, CG and FlashFS with XeLL

optionally, the system update container (su20076000_00000000) can be provided for flash files
and backed by files automatically extracted from nanddump.bin or found in /common and <build>/flashfs folders
instead of putting all files in this folder

note, with bls the following is true (before calculating CRC for an ini):
- the file is truncated to the u32 size found at offset 0xC
- CB/CB_A/CB_B 0x0 fill: @0x10 for 0x30 bytes
- CD 0x0 fill: @0x10 for 0x10
- CE 0x0 fill: @0x10 for 0x10
- CF 0x0 fill: @0x20 for 0x210
- CG 0x0 fill: @0x10 for 0x10

note, for CB_X and Payloads (xell_1f, etc), the CRC should be left blank to account for changes.