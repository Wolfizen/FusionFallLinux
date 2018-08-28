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

### Installing

First, download and install the following packages: `wine-staging`, `winetricks`.  
Then, run the installer: `$ ./FusionFallRetro_Install.sh`  
Finally, use either the .desktop file or the .sh file (your preference!) to start the launcher.
