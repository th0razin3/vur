# Tuner for Void Linux

<p align="center"><img src="https://codeberg.org/th0razin3/vur/raw/branch/main/srcpkgs/tuner/tuner.png"></p>

Tuner is a minimalist radio station player. Discover and Listen to your favourite internet radio stations. Tuner uses the community-driven radio station catalog [radio-browser.info](https://www.radio-browser.info/).

For more info, please visit [codeberg.org/tuner/tuner](https://web.archive.org/web/20240414125106/https://codeberg.org/tuner/tuner).

## How do I install it?

You can use the prebuilt binaries in the releases page, or you can build your own. Download this repository (repo), copy/paste the `srcpkgs` folder in your local `void-packages` cloned repo (from [here](https://github.com/void-linux/void-packages)), run `./xbps-src pkg tuner` and wait for the building process to end. Afterwards, you can install the application with `sudo xbps-install --repository hostdir/binpkgs tuner`. If you've donwloaded the prebuilt packages from the releases page, you can install the application with `sudo xbps-install --repository /path/to/extracted/files tuner`.