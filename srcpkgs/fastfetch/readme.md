# Fastfetch for Void Linux

<p align="center"><img src="https://codeberg.org/th0razin3/vur/raw/branch/main/srcpkgs/fastfetch/fastfetch.png"></p>

Fastfetch is a neofetch-like tool for fetching system information and displaying them in a pretty way. It is written mainly in C, with performance and customizability in mind. Currently, Linux, Android, FreeBSD, MacOS and Windows 7+ are supported.

## Notes

The binaries in the releases are built with no additional dependencies listed [here](https://github.com/fastfetch-cli/fastfetch/wiki/Dependencies). So, basically, these binaries don't have any of the "extended" features that Fastfetch has (like showing the distro's logo in the terminal with an actual image). If you don't like that, build Fastfetch from source with your own preference.

## How do I install it?

You can use the prebuilt binaries in the releases page, or you can build your own. Download this repository (repo), copy/paste the `srcpkgs` folder in your local `void-packages` cloned repo (from [here](https://github.com/void-linux/void-packages)), run `./xbps-src pkg fastfetch` and wait for the building process to end. Afterwards, you can install the application with `sudo xbps-install --repository hostdir/binpkgs fastfetch`. If you've donwloaded the prebuilt packages from the releases page, you can install the application with `sudo xbps-install --repository /path/to/extracted/files fastfetch`.