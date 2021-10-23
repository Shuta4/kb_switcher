# Keyboard switcher for X11
Convenient way to switch keyboard layout with `Ctrl+Shift` or
any other combination.

[Workaround for Wayland](https://github.com/Shuta4/keyboard_layout_switcher)

## Why?
Xorg xserver have an [issue](https://gitlab.freedesktop.org/xorg/xserver/-/issues/258).
In short: if you set hotkey for layout switch to `ctrl+shift`
another hotkeys like `ctrl+shift+*` will not work. 
It's really annoying when you have used `ctrl+shift` for a lot of years on windows
and now need to change it to something else.

## Usage
### Installation
1. Install `python` and `pip` (search net for HOWTO).
2. Install python requirements: `sudo pip -r install requirements`.
3. Install `xkb-switch` with your package manager.
4. Place script in right place: `sudo cp kb_switcher /usr/bin/`
5. Run it: `kb_switcher` and enjoy nice switching.

### Configuration
You can change hotkeys and command to execute by editing `kb_switcher` script's
`key_combinations` and `cmd` variables.

### Autostart
Use your DE's autostart settings or just put `kb_switcher &` to your `~/.xinitrc`.

### Stop
`pkill kb_switcher`

### Remove
1. Remove script from place where you copied it: `sudo rm -f /usr/bin/kb_switcher`.
2. Remove `xkb-switch` with your package manager.
3. Uninstall python requirements: `sudo pip -r uninstall requirements`

