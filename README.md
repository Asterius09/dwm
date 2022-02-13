# Description
Custom adaptation of w0ng's original configuration from 2010. dwm v6.2. Tuned for Arch Linux.

## Branches and patches
The master branch is the stable and working build configuration, and the development branch is only for test purposes (you can use it, but it isn't recommended since I update it regularly to test things). Color codes are from [StatusColors Patch](https://dwm.suckless.org/patches/statuscolors/) and I fixed the statusbar gap problem applying a patch manually. It's pretty much the raw DWM experience but with some minor tweaks for the custom configuration. My statusbar is linked [here](https://github.com/asterius09/dotfiles), will work out of the box with this DWM as it uses xsetroot to execute it. 

## Prerequisites 
Font used is [Terminus](https://sourceforge.net/projects/terminus-font/files/terminus-font-4.49/terminus-font-4.49.1.tar.gz/download) and [Siji](https://github.com/stark/siji) (for the glyphs). You'll need also the basic Xorg packages in order for DWM to work on your distro (xorg-xsetroot is necessary if you want to apply a statusbar). Some keybindings are set to scrot (screenshots) and mpd (music) services so you'll need those also. 

## Installation process
Process is simple, you only have to git clone the stable repository and compile it from source:
```sh
git clone https://github.com/asterius09/dwm
```
Then, compile it with administrator rights:
```sh 
sudo make clean install
```
### (Recommended) ###
Download and compile DMenu. Since I use the original and not a customized one you have to download it from the source repo:
```sh 
git clone https://git.suckless.org/dmenu
```

## Manual configuration process
If you want to manually apply patches or custom configurations, follow these steps:

  1. Modify config.def.h / dwm.c at your liking.
  2. Save all the files and delete config.h if it's present (or config.def.h will be ommited while compiling).
  3. Compile it from source.

This way you'll apply updates safely without errors or wrong files at patching. If you want to keep the original compiled revision of config.def.h, you can edit config.h as it will be the default configuration file when compiling.

## Screenshots
![DWM](preview.png "Preview of the custom desktop environment")

## Keybindings

### Basic ###

[Shift]+[Mod]+[Enter]   - launch terminal.<br />

[Mod]+[b]               - show/hide bar.<br />
[Mod]+[p]               - dmenu for running programs like the x-www-browser.<br />
[Mod]+[Enter]           - push acive window from stack to master, or pulls last used window from stack onto master.<br />

[Mod] + [j / k]         - focus on next/previous window in current tag.<br />
[Mod] + [h / l]         - increases / decreases master size.<br />

### Navigation ###

[Mod]+[2]               - moves your focus to tag 2.<br />
[Shift]+[Mod]+[2]       - move active window to the 2 tag.<br />

[Mod] + [i / d]         - increases / decreases number of windows on master.<br />
[Mod] + [, / .]         - move focus between screens (multi monitor setup).<br />
[Shift]+[Mod]+[, / .]   - move active window to different screen.<br />

[Mod]+[0]               - view all windows on screen.<br />
[Shift]+[Mod]+[0]       - make focused window appear on all tags.<br />
[Shift]+[Mod]+[c]       - kill active window.<br />
[Shift]+[Mod]+[q]       - quit dwm cleanly.<br />

### Layout ###

[Mod]+[t]               - tiled mode. []=<br />
[Mod]+[f]               - floating mode. ><><br />
[Mod]+[m]               - monocle mode. [M] (single window fullscreen)<br />

### Floating ###

[Mod]+[R M B]           - to resize the floating window.<br />
[Mod]+[L M B]           - to move the floating window around.<br />
[Mod]+[Space]           - toggles to the previous layout mode.<br />
[Mod]+[Shift]+[Space]   - to make an individual window float.<br />
[Mod]+[M M B]           - to make an individual window un-float.<br />

### Custom Keybindings ###

[Shift]+[Mod]+[+]       - Increases first card MASTER volume in 5%.<br />
[Shift]+[Mod]+[-]       - Decreases first card MASTER volume in -5%.<br />
[Shift]+[Mod]+[P]       - Pauses/Continues the actual MPD song (through mpc).<br />
[Shift]+[Mod]+[R]       - Puts mpc repeat mode on.<br />
[Shift]+[Mod]+[AvPag]   - Goes forward 1 song on the playlist.<br />
[Shift]+[Mod]+[RePag]   - Goes back 1 song on the playlist.<br />
