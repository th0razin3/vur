# OpenArena for Void Linux

<p align="center"><img src="https://codeberg.org/th0razin3/vur/src/branch/main/srcpkgs/OpenArena/OpenArena.png"></p>

OpenArena is a free and open-source 3D FPS (First Person Shooter) game. It's based on the open-source engine and game (Quake III Arena) originally published by id Software, then forked from ioquake3. The OpenArena project was established on August 19, 2005, one day after the id Tech 3 source code released under GNU GPL-2.0-or-later license.OpenArena was officially released for Microsoft Windows, Linux and macOS. Third parties have also ported the game to FreeBSD, OpenBSD, Android and iOS. The game was also unofficially ported to the Raspberry Pi.

## How do I install it?

Mind you, this is just a repack of the original binaries built by the developers of the game, so it's available in i686 (x86) and x86_64 (x64) flavors only. You can use the prebuilt binaries in the releases page, or you can build your own. Download this repository (repo), copy/paste the `srcpkgs` folder in your local `void-packages` cloned repo (from [here](https://github.com/void-linux/void-packages)), run `./xbps-src pkg OpenArena` and wait for the building (packaging) process to end. Afterwards, you can install the application with `sudo xbps-install --repository hostdir/binpkgs OpenArena`. If you've donwloaded the prebuilt packages from the releases page, you can install the application with `sudo xbps-install --repository /path/to/extracted/files OpenArena`.