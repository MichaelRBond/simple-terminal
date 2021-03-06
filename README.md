# st - simple terminal

st is a simple terminal emulator for X which sucks less.

## Notes about this fork

This is a fork of ST, the original repo can be found here: [https://git.suckless.org/st/](https://git.suckless.org/st/)

The original ST webpage is here: [https://st.suckless.org/](https://st.suckless.org/)

This fork has the following changes from version 0.8.1

### Patches applied

* Box Draw : Improves box drawing for NCurses applications : [https://st.suckless.org/patches/boxdraw/](https://st.suckless.org/patches/boxdraw/)
* Hide Cursor : Hides the mouse cursor when typing in the terminal : [https://st.suckless.org/patches/hidecursor/](https://st.suckless.org/patches/hidecursor/)
* Vert Center : Centers text on a line when line scale is modified : [https://st.suckless.org/patches/vertcenter/](https://st.suckless.org/patches/vertcenter/)

### Back Port changed

Additionally I've back ported several up-stream fixes for memory leaks and crashes that were not in the 0.8.1 release.
This was done because the patches I wanted to apply were not compatible with the newer commits, and it was less work to
backport the changes on the patched code than update the patches.

### Personal Customizations

* Modify the standard terminal blue color to be lighter, and more readbale
* Update the pixel size to be more readbale on HiDPI screens

## Requirements

In order to build st you need the Xlib header files.

## Installation

Edit config.mk to match your local setup (st is installed into
the /usr/local namespace by default).

Afterwards enter the following command to build and install st (if
necessary as root):

```bash
make clean install
```

## Running st

If you did not install st with make clean install, you must compile
the st terminfo entry with the following command:

```bash
tic -sx st.info
```

See the man page for additional details.

## Credits

* Forked from [https://st.suckless.org/](https://st.suckless.org/)
* Based on Aurélien APTEL aurelien.aptel@gmail.com bt source code.
