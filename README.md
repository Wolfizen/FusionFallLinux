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

First, download and install the following packages: `wine-staging`, `winetricks`, and optionally `dxvk` plus its Vulkan dependencies.  
Then, run the installer: `$ ./Standalone_Installer.sh`  
Finally, use either the .desktop file or the .sh file (your preference!) to start the launcher.

I have found that this game runs best with [DXVK](https://github.com/doitsujin/dxvk) installed. The script will report the status of DXVK and enable it automatically if detected. One can disable automatic installation by passing `-dxvk` as an argument, or force installation with `+dxvk`.

If you wish to modify the Wine installation folder from the default, override the `WINEPREFIX` environment variable before running. An example: `$ WINEPREFIX="$HOME/bin/FusionFall" ./Standalone_Installer.sh`

### Installing via Lutris

Lutris is an open-source Linux game manager. FusionFall Retro has an entry in their database, you can select it and install from there OR you can use my script directly. I publish any change I make here to Lutris, but there may still be differences - Lutris is an open platform and anyone can suggest changes.

To install via their database, first install the Lutris program, then open [FusionFall Retro](https://lutris.net/games/fusionfall-retro/) in their database and click "Install". It will open in Lutris and proceed to the installation.

To install directly, save `Lutris_Installer.yaml` locally and run: `$ lutris --install Lutris_Installer.yaml`.

### Known Problems on Linux

If the game is started with a resolution of more than 1920*1080px, some fonts might fail to load properly. To fix this, un-maximize the game during the Dexlabs loading screen, then bring it back to your preferred resolution once the game has finished loading and the world is visible.

When running the game without DXVK, several "Unexpected Error" popups may appear during game startup and loading. These do not prevent the game from running, and will not appear once the game has completed loading.

### Installing on a VM

Virtual Machines can run Windows games in Linux where other options do not work. FusionFall is not a demanding game and should run fine even on a low-power computer. I can run on max settings with my integrated Intel HD 520.

1. Download your favorite flavor of virtual machine. I prefer OracleBox.
2. Give the guest machine maximum video memory, and enable 2D/3D acceleration.
3. Install Windows. I tested with 10, anything 7 or later will work.
4. Download and install Microsoft Visual C++ Redistributable 2015 x86 AND x64.
5. Download and install Microsoft .NET Framework 4.7.2.
6. Run the installer. The launcher and game should start successfully.
7. If you have mouse movement issues ingame, I recommend disabling Mouse Integration for your VM and/or changing the input device to PS/2 mouse.
