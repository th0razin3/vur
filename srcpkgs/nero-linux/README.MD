# Nero Linux 4 (Nero Burning ROM) for Void Linux

![nero-linux_4 0 0 1_1](https://github.com/th0razin3/vur/assets/158844949/054b0953-95a6-4092-a6f0-f5b7c7d7c20a)

This is a port of the (now discontinued) Nero Burning ROM for Linux. Ahead Software AG (now Nero AG) made this Linux port of Nero Burning ROM about 20 years ago, with this version (the last one) being released in 2010. There are other burning applications out here, sure, but some of us like the look and feel of Nero Burning ROM, so even though this is a 13 year old piece of software, some might still like to use it. It still works on modern distros, and (of course, tested) in Void Linux.

## How do I install it?

You either clone this repo and copy the `srcpkgs` directory in the `void-packages` directory and build with xbps-src (`./xbps-src pkg nero-linux`), or you download the packaged version I made from the releases page and point xbps-install to install from a local repository (`sudo xbps-install --repository /path/to/extracted/files nero-linux`). Both i686 (x86) and x86_64 (x64) versions are packaged. No other architectures are supported unfortunately.

