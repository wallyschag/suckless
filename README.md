# Wally's suckless configs 
- Currently using...
    - dwm for my window manager
    - slstatus for my status bar
    - st for my terminal emulator
    - dmenu for my launch menu

## Changing configs
- Make all changes to config.def.h files for each respective application (dwm/, slstatus/, st/, dmenu/)
- The actual C programs for each application uses the config.mk file for definitions so run `$ make -B` in the root directory to copy the contents of config.def.h over to config.mk
- Run `$ sudo make clean install` in the root directory to compile the program and save changes
- Restart the program for changes to take effect

## Patching
- Requires patch -> `$ sudo pacman -S patch`
- `$ curl -O https://dwm.suckless.org/patches/{patch}.diff` to download the patch
- Run `$ patch -i {patch}.diff` to apply the patch to the program.
- WARNING: Patches alter the the source code, so it's important to have a backup somewhere of each root directory BEFORE Patching 
