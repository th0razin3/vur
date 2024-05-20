# PreSonus Studio One for Void Linux

<p align="center"><img src="https://codeberg.org/th0razin3/vur/raw/branch/main/srcpkgs/PreSonus-Studio-One/PreSonus-Studio-One.png"></p>

Studio One is a digital audio workstation (DAW) application, used to create, record, mix and master music and other audio, with functionality also available for video.

## Notes

The target OS for this version of Studio One is Ubuntu 24.04, which is why some libraries had to be taken from Ubuntu's repository (it doesn't work with the versions Void has in it's repos, tested). Also, Studio One is a Wayland only application, so tough luck for people still on X11. It does work through `weston` though. Install `weston-x11` in Void, run it from the terminal, run a Wayland terminal and type `PreSonus-Studio-One` in it, this will run Studio One.

## How do I install it?

Clone this repository, copy/paste the `srcpkgs` directory in your locally cloned `void-packages` repo (repository) and build (repackage) the application with `./xbps-src pkg PreSonus-Studio-One`. You can then install PreSonus Studio One with `sudo xbps-install --repository hostdir/binpkgs PreSonus-Studio-One`. Or, check the releases page in this repo for the latest repackaged version. You can install the Void Linux repack with `sudo xbps-install --repository /path/to/extracted/files PreSonus-Studio-One`. Unfortunatelly, only x64 builds/repackages are available (PreSonus only provides AMD64 binaries for Linux).