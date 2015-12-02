i3lock-color - improved screen locker
=====================================

*making i3lock's typing indicator color scheme configurable*

I added the following command line options:
* `--insidevercolor=rrggbbaa` -- Inside of the circle while the password is being verified
* `--insidewrongcolor=rrggbbaa` -- Inside of the circle when a wrong password was entered
* `--insidecolor=rrggbbaa` -- Inside of the circle while typing/idle
* `--ringvercolor=rrggbbaa` -- Outer ring while the password is being
* `--ringwrongcolor=rrggbbaa` -- Outer ring when a wrong password was entered
* `--ringcolor=rrggbbaa` -- Outer ring while typing/idle
* `--linecolor=rrggbbaa` -- Line separating outer ring from inside of the circle and delimiting the highlight segments
* `--textcolor=rrggbbaa` -- Text ("verifying", "wrong!")
* `--textattemptscolor=rrggbbaa` -- Text for the attempts counter
* `--keyhlcolor=rrggbbaa` -- Keypress highlight segments
* `--bshlcolor=rrggbbaa` -- Backspace highlight segments

All the colors have an alpha channel now. Please keep in mind that this was not intended when the program was originally written, so making thing transparent that weren't before can make it look strange.

### Examples:

i3lock --insidevercolor=0000a0bf --insidewrongcolor=ff8000bf --insidecolor=ffffffbf --ringvercolor=0020ffff --ringwrongcolor=4040ffff --ringcolor=404090ff --textcolor=ffffffff --linecolor=aaaaaaff --keyhlcolor=30ccccff --bshlcolor=ff8000ff

Ported from @eBrnd's great work at https://github.com/eBrnd/i3lock-color against i3lock 2.7 (latest)

Please submit all pull requests here, against https://github.com/kageurufu/i3lock-color

Original Readme
===============
i3lock is a simple screen locker like slock. After starting it, you will
see a white screen (you can configure the color/an image). You can return
to your screen by entering your password.

Many little improvements have been made to i3lock over time:

- i3lock forks, so you can combine it with an alias to suspend to RAM
  (run "i3lock && echo mem > /sys/power/state" to get a locked screen
   after waking up your computer from suspend to RAM)

- You can specify either a background color or a PNG image which will be
  displayed while your screen is locked.

- You can specify whether i3lock should bell upon a wrong password.

- i3lock uses PAM and therefore is compatible with LDAP etc.

Requirements
------------
- pkg-config
- libxcb
- libxcb-util
- libpam-dev
- libcairo-dev
- libxcb-xinerama
- libev
- libx11-dev
- libx11-xcb-dev
- libxkbcommon >= 0.5.0
- libxkbcommon-x11 >= 0.5.0

Running i3lock
-------------
Simply invoke the 'i3lock' command. To get out of it, enter your password and
press enter.

Upstream
--------
Please submit pull requests to https://github.com/i3/i3lock
