# Smile for Void Linux

<p align="center"><img src="https://codeberg.org/th0razin3/vur/raw/branch/main/srcpkgs/smile/smile.png"></p>

Smile is a simple emoji picker for Linux with custom tags support. It's build with Python 3 and GTK 3/4. The official releases are Flatpak only, but I decided to build and repackge this as a system wide package. The source is released [here](https://github.com/mijorus/smile).

## How do I install it?

Clone this repository, copy/paste the `srcpkgs` directory in your locally cloned `void-packages` repo (repository) and build (repackage) the application with `./xbps-src pkg smile`. You can then install Skype with `sudo xbps-install --repository hostdir/binpkgs smile`. Or, check the releases page in this repo for the latest repackaged version. You can install the Void Linux repack with `sudo xbps-install --repository /path/to/extracted/files smile`.