# th0razin3's Void Linux User Repository

This is my personal Void Linux user repository. Most xbps-src templates work, some are work in progress (it will be noted in a separate readme.md if the template is working or not).

Currently, this repository holds the following templates.

- DIE (Detect It Easy)
- Nero Linux 4 (Nero Burning ROM for Linux)
- numen
- ocenaudio
- Pale Moon (GTK2 and GTK3)
- Tuner
- Viber
- XnView MP

There is relevant info regarding each of the applications and/or quirks regarding packaging they might have in the adequate readme.md files in each of the subdirectories.

Regarding the package source files (versions and checksums), I can't always keep the versions and checksums up to date, so make sure you first check which is the newest version of the applications you'd like to package/repackage and change the `version` and `checksum` info in the template according to what's the newest.

## How do I use this repository?

Clone the `void-packages` repository from [here](https://github.com/void-linux/void-packages), then you clone this repository and copy/paste the `srcpkgs` directory into the `void-packages` directory and then package the application you like with `./xbps-src pkg foo-bar`. You don't need to have git installed in order to clone the repos (repositories), you could just use the GitHub web UI to clone them (`<> Code` --> `Download ZIP`or `...` --> `Dowload ZIP`). If errors occur, make sure to check whether the `version` and `checksum` info is correct (xbps-src will return the correct checksum if the checksum doesn't match the one in the template).

## Are there any packages/repacks available for download?

For some of the appliactions, yes, but for most, no. I will try and have builds/repacks available, but I make no promisses.

## Do you accept PRs?

Yes, but please be patient. I don't check this account as regularly as I do my main. It might be a few days before I check the PR. If I see that there is interest, I'll try and check it more regularly. Oh, and the main repo is on [codeberg.org](https://codeberg.org/th0razin3/vur), the rest are just push mirrors.
