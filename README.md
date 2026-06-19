# suckless
A repo dedicated to my suckless setup. As of now it contains
- dwm config.h

This is just a central place for me to keep track of the setup across devices

Updates to status bar:
- Fixed battery monitor, deactivated when not present
- Added volume indicator (pactl subscribe)

Updates to keybindings
- Dmenu spawns with Mod+d
- Firefox spawns with Mod+f
- Made placeholders for future keys

Fixed time advancement issue: the clock was not consitently updating. This is thought to be as a result of `date` output giving seconds with leading zeroes in the event that the seconds are less than 10. It Bash apparently interprets integers with leading zeroes as octal. This was corrected by using `%-S` rather than `%S` to find seconds.
