# XnView MP for Void Linux

<p align="center"><img src="https://codeberg.org/th0razin3/vur/raw/branch/main/srcpkgs/XnView-MP/XnView-MP.png"></p>

XnView MP is a versatile and powerful photo viewer, image management, image resizer. XnView is one of the most stable, easy-to-use, and comprehensive photo editors. All common picture and graphics formats are supported (JPEG, TIFF, PNG, GIF, WEBP, PSD, JPEG2000, OpenEXR, camera RAW, HEIC, PDF, DNG, CR2).

## Notes

This Void Linux template is a dirty hack (emphasis on the **dirty**).

Basically, `xbps-src` doesn't allow repackaging or buidling without a version number. Viber is closed source, so the best we could do is repackage. But, there's a problem. There is no version numbering on the website or in the filename of the downloaded .deb file (we're repacakaging from a Debian/Ubuntu package). So, this template basically doesn't conform to the `xbps-src` template standard (hence, the dirty hack). The version number is extracted from the .deb file on the fly, while `xbps-src` is running, which is not what `xbps-src` was meant to do. Hence, this template could stop working at any point (with new releases of `xbps-src`). For the time being, it works. Oh, and you need to have `tar` and `gzip` installed on your host machine (the one doing the repackaging) in order for this to work. These are common tools, so I presume you do have them installed, but just in case, here's a reminder: install them (`sudo xbps-install -Suv tar gzip`)!

If the checksum doesn't match, that probably means that they released a new version. See the error that `xbps-src` reports at the end of the failed packaging and correct the checksum with the one that `xbps-src` gives right before it exits (`checksum=0123456789abcdef`).

The `Keygen.exe` file is located in `/opt/XnView-MP/Keygen`. Yes, in order to register the software with the name that you'd like, you have to have Wine installed. The keygen is tested in Wine 9.6 and works OK. All you have to do is run `wine /opt/XnView-MP/Keygen/Keygen.exe` from a terminal. If you don't have Wine installed, use the name and serial provided in `Serial.txt` in the same directory (`/opt/XnView-MP/Keygen`). If you decide to remove XnView MP from your system, the `Keygen` directory will get removed as well, so you better make a copy of it if you'd like to keep the keygen.

## How do I install it?

Clone this repository, copy/paste the `srcpkgs` directory in your locally cloned `void-packages` repo (repository) and build (repackage) the application with `./xbps-src pkg XnView-MP`. You can then install XnView MP with `sudo xbps-install --repository hostdir/binpkgs XnView-MP`. Or, check the releases page in this repo for the latest repackaged version. You can install the Void Linux repack with `sudo xbps-install --repository /path/to/extracted/files XnView-MP`. Unfortunatelly, x64 builds/repackages are available (XnSoft only provides AMD64 binaries for Linux).