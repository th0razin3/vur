# Viber for Void Linux

<p align="center"><img src="https://codeberg.org/th0razin3/vur/raw/branch/main/srcpkgs/Viber/Viber.png"></p>

Viber, or Rakuten Viber, is a cross-platform voice over IP (VoIP) and instant messaging (IM) software application owned by Japanese multinational company Rakuten, provided as freeware for the Google Android, iOS, Microsoft Windows, Apple macOS and Linux platforms. Users are registered and identified through a cellular telephone number, although the service is accessible on desktop platforms without needing mobile connectivity. In addition to instant messaging it allows users to exchange media such as images and videos.

## Notes

This Void Linux template is a dirty hack (emphasis on the **dirty**).

Basically, `xbps-src` doesn't allow repackaging or buidling without a version number. Viber is closed source, so the best we could do is repackage. But, there's a problem. There is no version numbering on the website or in the filename of the downloaded .deb file (we're repacakaging from a Debian/Ubuntu package). So, this template basically doesn't conform to the `xbps-src` template standard (hence, the dirty hack). The version number is extracted from the .deb file on the fly, while `xbps-src` is running, which is not what `xbps-src` was meant to do. Hence, this template could stop working at any point (with new releases of `xbps-src`). For the time being, it works. Oh, and you need to have `bsdtar` and `ar` installed on your host machine (the one doing the repackaging) in order for this to work. These are common tools, so I presume you do have them installed, but just in case, here's a reminder: install them (`sudo xbps-install -Suv bsdtar ar`)!

Oh, and Viber is an AMD64 (x86_64) only application. Don't look at me, I'm as surprised as you... apparently Rakuten doesn't care about any other architecture... go bug them about it.

## How do I install it?

Clone this repository, copy/paste the `srcpkgs` directory in your locally cloned `void-packages` repo (repository) and build (repackage) the application with `./xbps-src pkg Viber`. You can then install Viber with `sudo xbps-install --repository hostdir/binpkgs Viber`. Or, check the releases page in this repo for the latest repackaged version. You can install the Void Linux repack with `sudo xbps-install --repository /path/to/extracted/files Viber`.

## How do I know if Viber is out of date?

You don't... the moment it stops working (connecting to the network), that means it's probably out of date (there may be an indicator somewhere in the UI, I have't checked or noticed to be honest). Run this template again in `xbps-src` (`./xbps-src pkg Viber`) and that will generate a new version of the package in `hostdir/binpkgs`. The repodata file will hold only the latest version, but the old version (if you hold that one) will still be in `hostdir/binpkgs`, so you better delete it (if you don't need it). Afterwards, just remove Viber from your PC/Laptop (`sudo xbps-remove -ROov Viber`), and then install it from `hostdir/binpkgs` (`sudo xbps-install --repository hostdir/binpkgs Viber` or `sudo xbps-install -R hostdir/binpkgs Viber`).

