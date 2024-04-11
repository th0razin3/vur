# DIE (Detect It Easy) for Void Linux

<p align="center"><img src="https://github.com/th0razin3/vur/assets/158844949/212215fb-48fa-44a9-a002-61b3d94b89c0"></p>

![DIE](https://github.com/th0razin3/vur/assets/158844949/212215fb-48fa-44a9-a002-61b3d94b89c0)

Detect It Easy, or abbreviated "DIE" is a program for determining types of files.

Many programs of the kind (PEID, PE tools) allow to use third-party signatures. Unfortunately, those signatures scan only bytes by the pre-set mask, and it is not possible to specify additional parameters. As the result, false triggering often occur. More complicated algorithms are usually strictly set in the program itself. Hence, to add a new complex detect one needs to recompile the entire project. No one, except the authors themselves, can change the algorithm of a detect. As time passes, such programs lose relevance without the constant support.

Detect It Easy has totally open architecture of signatures. You can easily add your own algorithms of detects or modify those that already exist. This is achieved by using scripts. The script language is very similar to JavaScript and any person, who understands the basics of programming, will understand easily how it works. Possibly, someone may decide the scripts are working very slow. Indeed, scripts run slower than compiled code, but, thanks to the good optimization of Script Engine, this doesn't cause any special inconvenience. The possibilities of open architecture compensate these limitations.

DIE exists in three versions. Basic version ("die"), Lite version ("diel") and console version ("diec"). All the three use the same signatures, which are located in the folder "db". If you open this folder, nested sub-folders will be found ("Binary", "PE" and others). The names of sub-folders correspond to the types of files. First, DIE determines the type of file, and then sequentially loads all the signatures, which lie in the corresponding folder. Currently the program defines the following types:

- MSDOS executable files MS-DOS
- PE executable files Windows
- ELF executable files Linux
- MACH executable files Mac OS
- Binary all other files

## How do I install DIE?

You can use the prebuilt binaries in the releases page, or you can build your own. Download this repository (repo), copy/paste the `srcpkgs` folder in your local `void-packages` cloned repo (from [here](https://github.com/void-linux/void-packages)), run `./xbps-src pkg DIE` and wait for the building process to end. Afterwards, you can install the application with `sudo xbps-install --repository hostdir/binpkgs DIE`. If you've donwloaded the prebuilt packages from the releases page, you can install the application with `sudo xbps-install --repository /path/to/extracted/files DIE`.