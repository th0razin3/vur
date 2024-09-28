# Stacher for Void Linux

<p align="center"><img src="https://codeberg.org/th0razin3/vur/raw/branch/main/srcpkgs/Stacher/Stacher.png"></p>

Stacher is a frontend (UI) for `yt-dlp`, combining the powerful functionality of the latter with the perks of working with a modern-looking GUI. It is important to mention that Stacher automatically installs `yt-dlp` on startup (renames it to `youtube-dl` afterwards), but you can configure it to use any fork application. You can also set your own paths to `yt-dlp` and `ffmpeg`, but if you have them installed as root (for all users), you have to start the application as root to set the path (it won't let you choose those binaries from the file picker if you're not running the application as root). The application features an elegant, black-themed GUI (which, for some reason, I was never able to find or configure for the Linux version), allowing you to paste the URL of the video to download in the dedicated field.

Stacher loads the video thumbnail and reveals its size, the download speed and the elapsed time before the download is completed. You can restart the download with a click and navigate to the source URL just as easily, from the right-click menu. The download location is easily accessible as well. A few additional settings allow you to modify the download location and change the filename of the output file automatically.

## Notes

This Void Linux template is a dirty hack (emphasis on the **dirty**).

Basically, `xbps-src` doesn't allow repackaging or buidling without a version number. Viber is closed source, so the best we could do is repackage. But, there's a problem. There is no version numbering on the website or in the filename of the downloaded .deb file (we're repacakaging from a Debian/Ubuntu package). So, this template basically doesn't conform to the `xbps-src` template standard (hence, the dirty hack). The version number is extracted from the .deb file on the fly, while `xbps-src` is running, which is not what `xbps-src` was meant to do. Hence, this template could stop working at any point (with new releases of `xbps-src`). For the time being, it works. Oh, and you need to have `bsdtar` and `ar` installed on your host machine (the one doing the repackaging) in order for this to work. These are common tools, so I presume you do have them installed, but just in case, here's a reminder: install them (`sudo xbps-install -Suv bsdtar ar`)!

Stacher is currently an AMD64 (x86_64) application, but if it goes open source, it can be ported to other architectures as well.

## How do I install it?

You can use the prebuilt binaries in the releases page, or you can build your own. Download this repository (repo), copy/paste the `srcpkgs` folder in your local `void-packages` cloned repo (from [here](https://github.com/void-linux/void-packages)), run `./xbps-src pkg Stacher` and wait for the building process to end. Afterwards, you can install the application with `sudo xbps-install --repository hostdir/binpkgs Stacher`. If you've downloaded the prebuilt packages from the releases page, you can install the application with `sudo xbps-install --repository /path/to/extracted/files Stacher`.