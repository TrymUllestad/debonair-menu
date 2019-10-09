dmenu - dynamic menu
====================
dmenu is an efficient dynamic menu for X. Originally made by the guys over at [suckless](https://tools.suckless.org/dmenu/), this is a minimally changed version of their software.

The applied patches are `password` and `lineheight`. I needed the `password` patch because I made a Bitwarden handler that took in my password via dmenu, the `lineheight` allows for a larger bar without having to increase font size.

Requirements
------------
In order to build dmenu you need the Xlib header files.


Installation
------------
Edit config.mk to match your local setup (dmenu is installed into
the /usr/local namespace by default).

Afterwards enter the following command to build and install dmenu:
```shell
$ sudo make clean install
```

Running dmenu
-------------
dmenu reads from standard input, allows users to select and search their desired item, and writes to standard output. Standard use is therefore as follows:
```shell
$ read-from-something | dmenu [-options] | receive-user-input
```
See the man page for details.
