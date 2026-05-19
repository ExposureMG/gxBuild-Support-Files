files that can be placed here:
-------------------------------
options.ini		- options file (settings can be entered on command line)
cpukey.txt 		- plain text file with ascii CPU key (not required if on command line or in options.ini)
cpukey.bin 		- binary cpukey used by some legacy apps

nanddump.bin	- dump of your consoles nand (can be a hacked image)
kv.bin			- keyvault (not required if using one from nanddump.bin)
smc.bin			- smc binary image (must be decrypted)
smc_config.bin	- smc configuration file

various security files, overrides files in system update container and nanddump.bin if present
should be provided decrypted
-----------------------------
crl.bin
dae.bin
extended.bin
odd.bin
secdata.bin

system settings, overrides files in nanddump.bin if present
not used if nomobiles is set to true
-----------------------------------------------------------
mobileB.bin
mobileC.bin
mobileD.bin
mobileE.bin
mobileF.bin
mobileG.bin
mobileH.bin

bootloader overrides, takes priority over files in build folder and common folder.
will be overriden by files in NAND unless nonandbl option is used
valid types: CB, CBA, CBB, CD, CE, CF, CG, SB, SC, SD, SE, SF, SG
should be provided decrypted
-----------------------------
<TYPE>_<version>.bin

not implemented
------------------------
Statistics.settings
Manufacturing.data
blmod.bin       - customization file to assist better glitch timing

