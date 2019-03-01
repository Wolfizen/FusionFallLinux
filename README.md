# FusionFallLinux
Tools to run FusionFall on Linux

[FusionFall](https://en.wikipedia.org/wiki/Cartoon_Network_Universe:_FusionFall) is a MMO based
on Cartoon Network's shows and characters. [FusionFall Universe](https://www.fusionfalluniverse.com/)
is a community dedicated to bringing back this game, as the official servers were shut down in 2013.

This repo hosts my work on getting the FusionFall Universe releases to run on Linux.

## Legacy
As of now, no launcher or runnable game has ever been released for Legacy.

## Retro
I have developed an installer script that sets up the necessary environment for FusionFall Retro to run.
It creates a wineprefix with the appropriate libraries, runs the FusionFall installer, and provides both a
.sh and .desktop file to start the launcher.

### Installing via a shell script

First, download and install the following packages: `wine-staging`, `winetricks`.  
Then, run the installer: `$ ./FusionFallRetro_Install.sh`  
Finally, use either the .desktop file or the .sh file (your preference!) to start the launcher.

If you wish to modify the Wine insllation folder from the default, override `WINEPREFIX` before 
running.  
An example: `$ WINEPREFIX="$HOME/bin/FusionFall" ./FusionFallRetro_Install.sh`

### Installing via Lutris

Lutris is an open-source Linux game manager. FusionFall Retro has an entry in their database, you can select it and install from there OR you can use my script directly. I publish any change I make here to Lutris, but there may still be differences - Lutris is an open platform and anyone can suggest changes.

To install via their database, first install the Lutris program, then open [FusionFall Retro](https://lutris.net/games/fusionfall-retro/) in their database and click "Install". It will open in Lutris and proceed to the installation.

To install directly, save `Lutris_Installer.yaml` locally and run: `$ lutris -i Lutris_Installer.yaml`.
