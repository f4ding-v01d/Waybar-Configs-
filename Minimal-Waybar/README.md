# Minimal Waybar

A clean, flat, no-frills [Waybar](https://github.com/Alexays/Waybar) configuration for Hyprland. No pills, no boxes, no gradients — just plain monospace text floating on a transparent bar.

Part of the [Waybar-Configs-](https://github.com/f4ding-v01d/Waybar-Configs-) collection.

![Preview](assets/preview.png)

## Features

- Fully transparent background, thin 22px bar
- Flat text modules — no borders, no pill backgrounds
- Hyprland workspaces that only appear when they actually hold a window
- Live clock, CPU / memory / temperature stats
- Network + volume control (via `wpctl`, no GUI dependency)
- Power profile switcher (click to cycle performance / balanced / power-saver)
- Battery indicator with warning/critical states
- System tray

## Preview

| Element | Behavior |
|---|---|
| Workspaces | Shown only when occupied, active workspace in white |
| Clock | Center, updates every second |
| Volume | Left-click to mute, scroll to adjust ±5% |
| Power profile | Click to cycle profiles |
| Battery / Network | Turns red on critical / disconnected states |

## Requirements

- [Waybar](https://github.com/Alexays/Waybar) (built with Hyprland support)
- Hyprland
- [JetBrainsMono Nerd Font](https://www.nerdfonts.com/font-downloads)
- `wpctl` (comes with PipeWire/WirePlumber — default on most modern setups)
- `power-profiles-daemon` (optional, for the power profile module)

## Installation

This config lives inside the `Minimal-Waybar-Config(V1)` folder of the repo, so clone the whole repo first, then copy just this folder's files:

```bash
git clone https://github.com/f4ding-v01d/Waybar-Configs-.git
cd "Waybar-Configs-/Minimal-Waybar-Config(V1)"
cp config.jsonc ~/.config/waybar/config.jsonc
cp style.css ~/.config/waybar/style.css
killall waybar && waybar &
```

> Note the folder name has spaces and parentheses (`Minimal-Waybar-Config(V1)`), so always quote the path in `cd`/`cp` commands, e.g. `cd "Waybar-Configs-/Minimal-Waybar-Config(V1)"`.

## Customization

All colors live at the top of `style.css` as plain hex values inline on each selector — no CSS variables, so just search-and-replace to retheme. Module order and behavior is controlled in `config.jsonc` under `modules-left` / `modules-center` / `modules-right`.

## License

MIT — use it, break it, rice it however you like.
