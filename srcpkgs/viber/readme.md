# Viber for Void Linux

<p align="center"><img src="https://codeberg.org/th0razin3/vur/raw/branch/main/srcpkgs/viber/viber.png"></p>

Viber, or Rakuten Viber, is a cross-platform voice over IP (VoIP) and instant messaging (IM) software application owned by Japanese multinational company Rakuten, provided as freeware for the Google Android, iOS, Microsoft Windows, Apple macOS and Linux platforms. Users are registered and identified through a cellular telephone number, although the service is accessible on desktop platforms without needing mobile connectivity. In addition to instant messaging it allows users to exchange media such as images and videos.

## Notes

This Void Linux template is a dirty hack. Basically, `xbps-src` doesn't allow repackaging or buidling without a version number. Viber is closed source, so the best we could do is repackage. But, there's a problem. There is no version numbering on the website or in the filename of the dwnloaded .deb file (we're repacakaging from a Debian/Ubuntu package). So, this template basically doesn't conform to the `xbps-src` template standard (hence, the dirty hack). The version number is extracted from the .deb file on the fly, while `xbps-src` is running, which is not what `xbps-src` was meant to do. Hence, this template could stop working at any point (with new releases of `xbps-src`). For the time being, it works. You will might also notice that this themplate downloads the .deb file twice. This is completely normal: the first time is for the version number, the second time is for the actual repackaging of the application. I could have probably made the template download the .deb file only once, but that would require a lot more work and... well, bandwidth is cheap nowadays, so... sorry, but I did the best I could in an afternoon's work.

## How do I install it?

Clone this repository, copy/paste the `srcpkgs` directory in your locally cloned `void-packages` repo (repository) and build (repackage) the application with `./xbps-src pkg vibe`. You can then install ocenaudio with `sudo xbps-install --repository hostdir/binpkgs viber`. 

## How do I know if Viber is out of date?

You don't... the moment it stops working, that means it's probably out of date (there may be an indicator somewhere in the UI, I have't checked or noticed to be honest). Run this template again in xbps



## How do I know if Viber is out of date?

You don't... short of downloading the Debian package manually, unpacking it and checking the binary's version, there is no way of knowing. You use it till it stops connecting to the Viber network because it's really out of date and then update the template (you'll need a new SHA256 checksum, but xbps-src will provide that in an error when building the package, if the one in this template is not valid), repackage Viber again, use one of the methods described above to update the install and that is basically it.

Viber may also inform you that it's out of date (upper left corner I believe), but if it's still connecting to the Viber network and you really don't need any new feature it might have, I'd leave it be. Though, of course, the choice is yours.

## Why is the template x64 only?

Go bug Viber about that. They only provide native binaries for Ubuntu, which has dropped all 32-bit support, inlcuing x86.

