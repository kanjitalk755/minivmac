Mini vMac runs emulation and drawing in a single thread.
Because of that, if drawing is blocked for some reason, the emulation speed will drop.
So I tried to separate the drawing to another thread in the macOS/SDL2 version.
Try if the CPU load does not reach 100% even with the speed setting "All out".

preparation:
$ brew install sdl2

example of how to build:
$ cc -o tool setup/tool.c
$ ./tool -t mcar -m II -api sd2 -speed a -as 0 | sh
$ xcodebuild

----------------

MnvM_b37: README
Paul C. Pratt
www.gryphel.com
July 27, 2005


MnvM_b37 is the build system for Mini vMac,
a miniature Macintosh emulator.

Further information may be found at
"https://www.gryphel.com/c/minivmac/".


You can redistribute MnvM_b37 and/or modify it under the terms
of version 2 of the GNU General Public License as published by
the Free Software Foundation.  See the included file COPYING.

MnvM_b37 is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
license for more details.
