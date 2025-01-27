# Bezelproject for Linux

A modified script of the BezelProject to allow for compatibility with rk3326 devices running ArkOS, TheRA, or RetroOZ. Requires dialog and imgp which will be installed on first run of the script if not already available. It also assumes a retroarch and retroarch32 configuration folders are located in the ~/.config folder.

To manually install dialog and imgp on Ubuntu/Debian Linux use ***sudo apt update -y && sudo apt install -y dialog imgp***.

-------
OVERVIEW

The Bezel Project Bezel Utility menu.

This utility will provide a downloader for Retroarch system bezel packs.

This utility provides a download for a bezel pack for a system and includes a PNG bezel file for every ROM for that system.  The download will also include the necessary configuration files needed for Retroarch to show them.

Periodically, new bezel packs are completed and you will need to run the script updater to download the newest version to see these additional packs.

***NOTE***
To have global support, these bezel packs will only work if the ROMs you are using are named according to the No-Intro naming convention used by EmuMovies/HyperSpin.

Systems with shared Retroarch cores and filenames: 
Only one bezel can exist for a specific game name, so systems that share the same Retroarch core and rom filename will use the same bezel.

-------
INSTALLATION

Before downloading, make sure bezels are enabled in retroarch by going to **Settings>On-Screen Display>Display Overlay** and setting it to "ON".

Do the following:

* Click on the green code button above and download the zip.
* Open the zip, then click into the `BezelProject-for-rk3326-master` folder and copy the BezelProject folder to /roms/tools.  The .sh file can be installed in the BezelProject folder or in the /roms/tools folder.
   * For ArkOS on the RG351V or RG351MP, if SD2 is being used for roms, installation must be in /roms2/tools/. The .sh file can be installed in the BezelProject folder or in the /roms2/tools folder.
* Run BezelProject.sh from ArkOS through Options > Tools system menu.

-------
UNINSTALL

NOTE: This modified script only uninstalls the bezels, and not the .cfg files in your config folder. To uninstall those, you'll have to do it manually. 

To manually remove The Bezel Project, delete the following directories.

/roms/_overlays/ArcadeBezels (or /roms2/_overlays/ArcadeBezels if using ArkOS on a device that supports a second sd card and you've activated that)

/roms/_overlays/GameBezels (or /roms2/_overlays/GameBezels if using ArkOS on a device that supports a second sd card and you've activated that)

Edit the retroarch.cfg located in the main directory (I recommend making a backup first):

~/.config/retroarch/

In retroarch, disable overlays by going to Settings>On-Screen Display>Display Overlays, and setting it to "OFF"

To remove the Retroarch game override config files, delete the core named folders located here:

~/.config/retroarch/config/(core named folder)

-------
Supported cores

**Arcade**: lr-mame2003, lr-mame2010, lr-fba

**Atari 2600**: lr-stella

**Atari 5200**: lr-atari800

**Atari 7800**: lr-prosystem

**ColecoVision**: lr-bluemsx

**GCE Vectrex**: lr-vecx

**NEC PC Engine CD**: lr-beetle-pce-fast

**NEC PC Engine**: lr-beetle-pce-fast

**NEC SuperGrafx**: lr-beetle-supergrafx

**NEC TurboGrafx-CD**: lr-beetle-pce-fast

**NEC TurboGrafx-16**: lr-beetle-pce-fast

**Nintendo 64**: lr-Mupen64plus

**Nintendo Entertainment System**: lr-fceumm, lr-nestopia

**Nintendo Famicom Disk System**: lr-fceumm, lr-nestopia

**Nintendo Famicom**: lr-fceumm, lr-nestopia

**Nintendo Game Boy**: lr-gambatte, lr-mgba

**Nintendo Game Boy Color**: lr-gambatte, lr-mgba

**Nintendo Super Famicom**: lr-snes9x, lr-snes9x2010

**Sega 32X**: lr-picodrive, lr-genesis-plus-gx

**Sega CD**: lr-picodrive, lr-genesis-plus-gx

**Sega Genesis**: lr-picodrive, lr-genesis-plus-gx

**Sega Master System**: lr-picodrive, lr-genesis-plus-gx

**Sega Mega Drive**: lr-picodrive, lr-genesis-plus-gx

**Sega Mega Drive Japan**: lr-picodrive, lr-genesis-plus-gx

**Sega SG-1000**: lr-genesis-plus-gx

**Sony PlayStation**: lr-pcsx-rearmed

**Super Nintendo Entertainment System**: lr-snes9x, lr-snes9x2010
