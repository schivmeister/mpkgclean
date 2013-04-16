mpkgclean
=========

This is a simple (and dumb) cache cleaner for `makepkg`, the
[pacman](https://www.archlinux.org/pacman/) package generator. It removes
all but the latest `pacman` binary package in a directory of multiple
packages, and is intended to accommodate those who use `PKGDEST`. It can be
run from any directory and will correctly process only `*.pkg.tar.[gx]z`
files.

To use, simply run `mpkgclean` by itself in a relevant directory. If you
are afraid of losing files, test it on a copy of the directory first.

Example Output
--------------
Directory with mixed packages:

	~$ mpkgclean
	Getting rid of old package formats...done
	Cleaning kmymonkey [1.4.1-1 -> 1.4.1-2] (i686)
	Cleaning gmymonkey [1.3-2 -> 1.3.1-1] (any)
	Cleaning furbypony [0.4.2-1 -> 0.5.0-2] (x86_64)
	Cleaning furbydonkey [0.10.1-1 -> 0.12.0-1] (any)

Directory with no packages or only single versions of packages:

	~$ mpkgclean
	Getting rid of old package formats...none found
	All clear, nothing to clean.

Known issues:

 * `*.sig` files will pollute output
 * Removal of older (gz) format is silent
