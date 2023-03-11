# sway-interactive-screenshot

sway-interactive-screenshot is as simple bash script to take screenshot with ease on sway. Just launch the script and it will ask you what you want to take a screenshot.

**This is a fork of [sway-interactive-screenshot](https://github.com/moverest/sway-interactive-screenshot) that simply places `HEAD` before the [Switch to Fuzzel](https://github.com/moverest/sway-interactive-screenshot/commit/c799936eb20b2a222690b7e5d999b3f28bdd94a9) commit. A commit which resulted in a switch away from Rofi to a picker with very limited theming functionality. The reasoning was Rofi's poor Wayland support, which is in a way entirely valid were it not for [lbonn's rofi for wayland](https://github.com/lbonn/rofi).**

## Install

If you are using Archlinux, you can install sway-interactive-screenshot with the AUR package [`sway-interactive-screenshot`](https://aur.archlinux.org/packages/sway-interactive-screenshot) (e.g. `yay -S sway-interactive-screenshot`).

## Dependencies

- `swaywm` obviously
- `jq` to parse `swaymsg` JSON response that lists windows
- `rofi` to prompt what you want to take a screenshot of
- `grim` to take the screenshot
- `slurp` to select an area on the screen
- [`swappy`](https://github.com/jtheoof/swappy) (optional) to edit the captured screenshot
- `notify-send` to send a notification to notification daomon (such as [`mako`](https://github.com/emersion/mako))
- `wl-copy` to copy the screenshot to the clipboard

## Bind it to the `Print` key

To bind this script to the `Print` key, just add this to your `~/.config/sway/config`:

```
bindsym Print exec /path/to/sway-interactive-screenshot
```

## Settings

By default, `sway-interactive-screenshot` saves the screenshots in the home directory. You can change that by setting the `SWAY_INTERACTIVE_SCREENSHOT_SAVEDIR` environment variable to another directory.
