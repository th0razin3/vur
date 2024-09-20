# Pale Moon (GTK2) for Void Linux

<p align="center"><img src="https://codeberg.org/th0razin3/vur/raw/branch/main/srcpkgs/palemoon-gtk2/palemoon.png"></p>

Pale Moon is an Open Source, Goanna-based web browser available for various operating systems including Microsoft Windows, Mac OS and Linux (with contributed other operating system support), focusing on efficiency and customization.

Pale Moon offers you a browsing experience in a browser completely built from its own, independently developed source that has been forked off from Firefox/Mozilla code a number of years ago, with carefully selected features and optimizations to improve the browser's stability and user experience, while offering full customization and a growing collection of extensions and themes to make the browser truly your own.

## How do I install it?

Clone this repository, copy/paste the `srcpkgs` directory in your locally cloned `void-packages` repo (repository) and build (repackage) the application with `./xbps-src pkg palemoon-gtk2`. You can then install Pale Moon with `sudo xbps-install --repository hostdir/binpkgs palemoon-gtk2`. Or, check the releases page in this repo for the latest repackaged version. You can install the Void Linux repack with `sudo xbps-install --repository /path/to/extracted/files palemoon-gtk2`.

Oh, and you can't have both GTK2 and GTK3 builds of Pale Moon installed. If you have one or the other installed and you'd like to switch, first you need to uninstall the build you have installed. I could probably make a repack that will allow both versions to be installed, but I don't see a point to be honest.

## A note for the Pale Moon developers, if they happen to stumble upon this repack

This is just a repack, not a rebuild of Pale Moon. No third party libraries have been added to this repack. I'm using Steven Pusser's Debian builds to make this repack. Nothing has been changed in the binaries, except the distribution (distro) this repack targets, i.e. Void Linux.