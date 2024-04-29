# Viber for Void Linux

<p align="center"><img src="https://codeberg.org/th0razin3/vur/raw/branch/main/srcpkgs/viber/viber.png"></p>

Viber, or Rakuten Viber, is a cross-platform voice over IP (VoIP) and instant messaging (IM) software application owned by Japanese multinational company Rakuten, provided as freeware for the Google Android, iOS, Microsoft Windows, Apple macOS and Linux platforms. Users are registered and identified through a cellular telephone number, although the service is accessible on desktop platforms without needing mobile connectivity. In addition to instant messaging it allows users to exchange media such as images and videos.

## Notes

This Void Linux template is a dirty hack. Basically, `xbps-src` doesn't allow repackaging or buidling without a version number. Viber is closed source, so the best we could do is repackage. But, there's a problem. There is no version numbering on the website or in the filename of the dwnloaded .deb file (we're repacakaging from a Debian/Ubuntu package). So, this template basically doesn't conform to the `xbps-src` template standard (hence, the dirty hack). The version number is extracted from the .deb file on the fly, while `xbps-src` is running, which is not what `xbps-src` was meant to do. Hence, this template could stop working at any point (with new releases of `xbps-src`). For the time being, it works.

You will might also notice that this themplate downloads the .deb file twice. This is completely normal: the first time is for the version number, the second time is for the actual repackaging of the application. I could have probably made the template download the .deb file only once, but that would require a lot more work and... well, bandwidth is cheap nowadays, so... sorry, but I did the best I could in an afternoon's work.

Oh, and Viber is an AMD64 (x86_64) only application. Don't look at me, I'm as surprised as you... apparently Rakuten don't care about any other architecture... go bug them about it.

## How do I install it?

Clone this repository, copy/paste the `srcpkgs` directory in your locally cloned `void-packages` repo (repository) and build (repackage) the application with `./xbps-src pkg vibe`. You can then install ocenaudio with `sudo xbps-install --repository hostdir/binpkgs viber`. I don't repackage Viber, it's way too big at the time (they now have to build/package binaries for Wayland and X.org in a single package, so that takes a lot of space).

## How do I know if Viber is out of date?

You don't... the moment it stops working, that means it's probably out of date (there may be an indicator somewhere in the UI, I have't checked or noticed to be honest). Run this template again in `xbps-src` (`./xbps-src pkg viber`) and that should overwrite (delete) the old version of the package in `hostdir/binpkgs` and package the new one. Afterwards, just remove Viber from your PC/Laptop (`sudo xbps-remove -ROov viber`), and then install it from `hostdir/binpkgs` (`sudo xbps-install --repository hostdir/binpkgs viber` or `sudo xbps-install -R hostdir/binpkgs viber`).

