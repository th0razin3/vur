# XnView MP for Void Linux

<p align="center"><img src="https://codeberg.org/th0razin3/vur/raw/branch/main/srcpkgs/XnView-MP/XnView-MP.png"></p>

XnView MP is a versatile and powerful photo viewer, image management, image resizer. XnView is one of the most stable, easy-to-use, and comprehensive photo editors. All common picture and graphics formats are supported (JPEG, TIFF, PNG, GIF, WEBP, PSD, JPEG2000, OpenEXR, camera RAW, HEIC, PDF, DNG, CR2).

## Notes

The `Keygen.exe` file is located in `/opt/XnView/Keygen`. Yes, in order to register the software with the name that you'd like, you have to have Wine installed. The keygen is tested in Wine 9.6 and works OK. All you have to do is run `wine /opt/XnView/Keygen/Keygen.exe` from a terminal. If you don't have Wine installed, use the name and serial provided in `Serial.txt` in the same directory (`/opt/XnView/Keygen`). If you decide to remove XnView MP from your system, the `Keygen` directory will get removed as well, so you better make a copy of it if you'd like to keep the keygen.

Currently, there is no way to tell which version the template is downloading from the site of the developer. They don't use version numbering in their releases. So, if the checksum doesn't match, that probably means that they releases a new version. Visit the XnView MP website, see what the latest version is (they do state the latest version on the website) and correct the template with the adequate version number (`version=x.y.z`). You'll also need to correct the chekcum in the template (`checksum=0123456789abcdef`).

## How do I install it?

Clone this repository, copy/paste the `srcpkgs` directory in your locally cloned `void-packages` repo (repository) and build (repackage) the application with `./xbps-src pkg xnview-mp`. You can then install XnView MP with `sudo xbps-install --repository hostdir/binpkgs xnview-mp`. Or, check the releases page in this repo for the latest repackaged version. You can install the Void Linux repack with `sudo xbps-install --repository /path/to/extracted/files xnview-mp`. Unfortunatelly, x64 builds/repackages are available (XnSoft only provides AMD64 binaries for Linux).