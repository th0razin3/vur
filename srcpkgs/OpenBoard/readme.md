# OpenBoard for Void Linux

<p align="center"><img src="https://codeberg.org/th0razin3/vur/raw/branch/main/srcpkgs/OpenBoard/OpenBoard.png"></p>

OpenBoard is a free and open-source interactive whiteboard software compatible with any projector and pointing device. It was originally forked from Open-Sankoré in 2013 with the intention to focus on simplicity and stability. The license was upgraded from LGPL-2.0-only to GPL-3.0-only. Since version 1.3 it is using the more recent QT 5 framework instead of QT version 4. Open-Sankoré itself is based on the Uniboard software originally developed at the University of Lausanne (UL), Switzerland.

## How do I install it?

You can use the prebuilt binaries in the releases page, or you can build your own. Download this repository (repo), copy/paste the `srcpkgs` folder in your local `void-packages` cloned repo (from [here](https://github.com/void-linux/void-packages)), run `./xbps-src pkg OpenBoard` and wait for the building process to end. Afterwards, you can install the application with `sudo xbps-install --repository hostdir/binpkgs OpenBoard`. If you've donwloaded the prebuilt packages from the releases page, you can install the application with `sudo xbps-install --repository /path/to/extracted/files OpenBoard`.