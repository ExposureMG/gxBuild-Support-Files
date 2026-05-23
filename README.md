# gxBuild Support Files

Required folders and files to run gxBuild. Based on xeBuild 1.21 support files.

>[!CAUTION]
> * The patches are from xeBuild 1.21
> * The RGLoader patches are from the last version i can find before the repo was archived
> * If you have updated versions please open a PR


### Patches / Payloads

- [RGLoader.xex](https://github.com/J-Runner-With-Extras/RGLoader-XEX) by Team RGLoader and Team J-Runner

- [RGLoader Patches](https://github.com/RGLoader/RGLoader-Patches) by Team RGLoader

- [DashLaunch 3.21](https://digiex.net/threads/dash-launch-3-21-for-jtag-rgh-xbox-360s-running-freeboot.11024/) by c0z

- [xeBuild 1.21 Patches](https://digiex.net/threads/xebuild-1-21-latest-dashboard-system-update-builder-for-jtag-rgh-xbox-360.7278/) by c0z?

- [XeLL-Reloaded](https://github.com/Free60Project/xell-reloaded) by Free60 (Latest as of 20/5/26)

- [RGH1.3 Patches](https://github.com/wurthless-elektroniks/RGH1.3) by wurthless-elektroniks

- gxBuild JSON Patches

- gxBuild GXS2 Patches

## Structure

### Build Folders (-d)

Build Folders (numbered) -> Kernel / Dashboard Versions

\<Build Folder\>/bin -> Patches unique to the Build Folder

\<Build Folder\>/flashfs -> Optional folder to keep loose FlashFS assets

\<Build Folder\>/payloads -> Optional folder to override common payloads folder

\<Build Folder\>/smc -> Optional folder to override common smc folder


### SMC

smc -> SMC binaries common to all versions

smc/bin -> SMC JSON Patches


### Other

mydata -> User-specific override files

payloads -> Files found in INI payload section, common to all versions

common -> Bootloader files common to all versions


## Glitch3 Info

- CB_X should be left without a CRC32, and named CBX.bin. This allows the CBX to easily be hot swapped in mydata or common folders.

- You could technically use a specific CB_X version with a CRC but afaik theres benefits and drawbacks to all of them


## Changes to INIs

- Payloads section is required for hacked images
