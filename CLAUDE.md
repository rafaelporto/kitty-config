# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

This is a personal [kitty terminal](https://sw.kovidgoyal.net/kitty/) configuration repository. It contains `kitty.conf`, theme files, and background images.

## Applying Changes

- **Reload config without restarting:** `Ctrl+Shift+F5` (noted in line 3 of kitty.conf)
- **Switch themes interactively:** `kitty +kitten themes` — this updates `current-theme.conf` and the `BEGIN_KITTY_THEME` block at the bottom of `kitty.conf`
- **List available fonts:** `kitty +list-fonts`

## Structure

- `kitty.conf` — main config file; heavily commented (kitty default template). Actual custom settings are sparse (font, theme include, background).
- `themes/` — 170+ `.conf` theme files (one per theme). Switch by changing the `include` line near the top of `kitty.conf`.
- `current-theme.conf` — managed by `kitty +kitten themes`; included at the bottom of `kitty.conf` inside `BEGIN_KITTY_THEME / END_KITTY_THEME` markers.
- `background-images/` — PNG/JPG wallpapers for the `background_image` setting.

## Key Configuration Points

**Font** (top of kitty.conf):
```
font_family CaskaydiaCove Nerd Font
font_size 24.0
```

**Theme** — two mechanisms coexist:
1. Manual `include ./themes/<name>.conf` near the top (several are commented out).
2. Kitty's built-in theme manager appends `include current-theme.conf` at the bottom — this takes precedence.

**Background image** — currently commented out:
```
# background_image ./background-images/druid-emblema-wallpaper.jpg
background_image_layout scaled
background_tint 0.9
```
To enable, uncomment the `background_image` line and point it to one of the files in `background-images/`.
