# Skype for Void Linux

<p align="center"><img src="https://codeberg.org/th0razin3/vur/raw/branch/main/srcpkgs/Skype/Skype.png"></p>

Skype is a proprietary telecommunications application operated by Skype Technologies, a division of Microsoft, best known for IP-based videotelephony, videoconferencing and voice calls. It also has instant messaging, file transfer, debit-based calls to landline and mobile telephones (over traditional telephone networks), and other features. It is available on various desktop, mobile, and video game console platforms.

## Notes

This Void Linux template is a dirty hack (emphasis on the **dirty**).

Basically, `xbps-src` doesn't allow repackaging or buidling without a version number. Skype is closed source, so the best we could do is repackage. But, there's a problem. Skype Technologies recently switched to a snap based only distribution of Skype. This basically means that there are no packages built for any platform, including Debian/Ubuntu. Version numbering and the download URL for the snap package is included in the Snapcraft store via the Snap Store API, but it needs to be extracted, thus we can't define the version number or the snap package download URL in the template. So, this template basically doesn't conform to the `xbps-src` template standard (hence, the dirty hack). The version number is extracted from the Snap Store API on the fly, while `xbps-src` is running. Hence, this template could stop working at any point (with new releases of `xbps-src`). For the time being, it works. Oh, and you need to have `curl` and `jq` installed on your host machine (the one doing the repackaging) in order for this to work. You can install them with `sudo xbps-install -Suv curl jq`.

There is a Skype template in the official Void repo, I know, but that template hasn't been updated in quite a while and apprently, whoever maintained it, isn't aware of the switch to a snap only distribution of Skype. That template doesn't even work any more because Microsoft has removed all `.deb` and `.rpm` packages from their download site, so the URL in `distfiles` won't work. You could probably get the latest `.deb` or `.rpm` package from archive.org and just change the URL in the `distfiles` variable, but that version will stop working with the Skype network sooner or later. As far as I know, this template doesn't interfere with what's in the official Void repository, but I can't be sure since I couldn't build the official repo version of Skype. In any case, if you're switching from the official repo version of Skype to this one, make sure you uninstall Skype first (`sudo xbps-remove -ROov skype`) and then install the version from this template.

Oh, and Skype is an AMD64 (x86_64) only application. Don't look at me, I'm as surprised as you... apparently Microsoft doesn't care about any other architecture... go bug them about it.

## How do I install it?

Clone this repository, copy/paste the `srcpkgs` directory in your locally cloned `void-packages` repo (repository) and build (repackage) the application with `./xbps-src pkg Skype`. You can then install Skype with `sudo xbps-install --repository hostdir/binpkgs Skype`. Or, check the releases page in this repo for the latest repackaged version. You can install the Void Linux repack with `sudo xbps-install --repository /path/to/extracted/files Skype`.