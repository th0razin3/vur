# numen for Void Linux

Numen is voice control letting you have full control of a Linux machine without needing to type. It empowers people who otherwise couldn't use their computers, and helps more avoid hand strain. Numen is free (libre) software and runs locally. You can view a video demonstration [here](https://web.archive.org/web/20240425125404/https://files.catbox.moe/hcd4ul.webm).

## Notes

Regarding the template, I am not the original author, the author of the project did all of the work (almost all), but it didn't make it in the official repos, the PR went stale and then the project author stopped using Void Linux and just closed the PR ([here](https://github.com/void-linux/void-packages/pull/39716) is the PR). So, I just decided to pick where he left off and did just a few minor corrections regarding how xbps-src handles the service run files.

## How do I install it?

You can use the prebuilt binaries in the releases page, or you can build your own. Download this repository (repo), copy/paste the `srcpkgs` folder in your local `void-packages` cloned repo (from [here](https://github.com/void-linux/void-packages)), run `./xbps-src pkg numen` and wait for the building process to end. Afterwards, you can install the application with `sudo xbps-install --repository hostdir/binpkgs numen`. If you've donwloaded the prebuilt packages from the releases page, you can install the application with `sudo xbps-install --repository /path/to/extracted/files numen`.