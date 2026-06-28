# suckless
A repo dedicated to my suckless setup. As of now it contains
- dwm config.h

This is just a central place for me to keep track of the setup across devices

## Updates to status bar:
- Fixed battery monitor, deactivated when not present
- Added volume indicator (pactl subscribe)
- Fixed time advancement issue: the clock was not consistently updating. This is thought to be as a result of `date` output giving seconds with leading zeroes in the event that the seconds are less than 10. It Bash apparently interprets integers with leading zeroes as octal. This was corrected by using `%-S` rather than `%S` to find seconds.

## Updates to dwm keybindings
- Dmenu spawns with Mod+d
- Firefox spawns with Mod+f
- Made placeholders for future keys
- Went back to Super+Shift+Return to spawn terminal with tmux
- Super+Shift+t spawns st without tmux open
- Added a binding for screenshots - Printscreen key (requires flameshot)


## Updates to st terminal emulator:
- changed font to `JetBrains Mono NL` (see installation instructions)
- updated dwm config.h to allow tmux to open by default at start of session

### JetBrains Mono NL installation instructions:

Before a `sudo make clean install` the font needs to be installed:

`$ /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/JetBrains/JetBrainsMono/master/install_manual.sh)`
`$ fc-cache -fv`

The font should then be available on st restart after a clean install.
