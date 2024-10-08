# ocenaudio for Void Linux

<p align="center"><img src="https://codeberg.org/th0razin3/vur/raw/branch/main/srcpkgs/ocenaudio/ocenaudio.png"></p>

ocenaudio is a closed-source, cross-platform, easy to use, fast and functional audio editor. It is the ideal software for people who need to edit and analyze audio files without complications. ocenaudio also has powerful features that will please more advanced users.

This software is based on Ocen Framework, a powerful library developed to simplify and standardize the development of audio manipulation and analysis applications across multiple platforms.

## How do I install it?

Clone this repository, copy/paste the `srcpkgs` directory in your locally cloned `void-packages` repo (repository) and build (repackage) the application with `./xbps-src pkg ocenaudio`. You can then install ocenaudio with `sudo xbps-install --repository hostdir/binpkgs ocenaudio`. Or, check the releases page in this repo for the latest repackaged version. You can install the Void Linux repack with `sudo xbps-install --repository /path/to/extracted/files ocenaudio`. Unfortunatelly, only an x64 (AMD64) version is available.
