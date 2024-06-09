# Amarok for Void Linux

<p align="center"><img src="https://codeberg.org/th0razin3/vur/raw/branch/main/srcpkgs/amarok/amarok.png"></p>

Amarok is a free and open-source music player for Linux, macOS, Windows, and other Unix-like operating systems. Amarok is part of the KDE project, but it is released independently of the central KDE Software Compilation release cycle. Amarok is released under the terms of the GPL-2.0-or-later.

Amarok supports a wide variety of music formats due to the use of audio engines. It can retrieve cover art information and lyrics from the internet. It includes a sidebar that displays the user's music collection, saved playlists, and internet radio stations on the left and the active playlist on the right. Amarok can also display the Wikipedia entry for the band or album in the sidebar. Other features include dynamic playlists, bookmarking, file tracking, and smooth fade-out settings.

## How do I install it?

You can use the prebuilt binaries in the releases page, or you can build your own. Download this repository (repo), copy/paste the `srcpkgs` folder in your local `void-packages` cloned repo (from [here](https://github.com/void-linux/void-packages)), run `./xbps-src pkg amarok` and wait for the building process to end. Afterwards, you can install the application with `sudo xbps-install --repository hostdir/binpkgs amarok`. If you've donwloaded the prebuilt packages from the releases page, you can install the application with `sudo xbps-install --repository /path/to/extracted/files amarok`.