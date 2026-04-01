# Kitty Configuration

Personal [kitty](https://sw.kovidgoyal.net/kitty/) terminal configuration.

## Font

**CaskaydiaCove Nerd Font** at size 24.

## Theme

Managed via `kitty +kitten themes`. The active theme is stored in `current-theme.conf` and included at the bottom of `kitty.conf`. Additional themes are available in the `themes/` directory.

## Background Images

Background wallpapers are stored in `background-images/`. To enable one, uncomment and set `background_image` in `kitty.conf`:

```conf
background_image ./background-images/druid-emblema-wallpaper.jpg
```

## Reload Config

`Ctrl+Shift+F5` — reloads kitty configuration without restarting.
