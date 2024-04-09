# th0razin3's Void Linux User Repository

This is my personal Void Linux user repository. Most xbps-src templates work, some are work in progress (it will be noted in a separate readme.md if the template is working or not).

Currently, this repository holds the following templates.
- Nero Linux 4 (Nero Burning ROM for Linux)
- Viber
- ocenaudio

There is relevant info regarding each of the applications and/or quirks regarding packaging they might have in the adequate readme.md files in each of the subdirectories.

Regarding the package source files (versions and checksums), I can't always keep the versions and checksums up to date, so make sure you first check which is the newest version of the applications you'd like to package/repackage and change the `version` and `checksum` info in the template according to what's the newest.

## How do I use this repository?

Clone the `void-packages` repository from [here](https://github.com/void-linux/void-packages), then you clone this repository and copy/paste the content into the `void-packages` repository and then package the application you like with ./xbps-src pkg foo-bar`. If errors occur, make sure to check whether the `version` and `checksum` info is correct (xbps-src will return the correct checksum if the checksum doesn't match the one in the template).
