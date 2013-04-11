mpkgclean
=========

This is a simple (and dumb) cache cleaner for `makepkg`, the `pacman` package
generator.¹ It removes all but the latest `pacman` binary package in a
directory of multiple packages, and is intended to accommodate those who
use `PKGDEST`. It can be run from any directory and will correctly process
only `*.pkg.tar.[gx]z` files.

To use, simply run `mpkgclean` by itself in a relevant directory. If you
are afraid of losing files, test it on a copy of the directory first.

¹ [https://www.archlinux.org/pacman/](https://www.archlinux.org/pacman/)
