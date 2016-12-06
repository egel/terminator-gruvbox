# Terminator gruvbox colors

A color theme for [terminator](http://www.tenshu.net/terminator/) using Pavel Pertsev’s [Gruvbox color scheme](https://github.com/morhetz/gruvbox).

## Screenshots
![gruvbox terminator](http://i.imgur.com/HjSy0Ga.png)

> Note: To make same look as on screenshot set below features:
> -   Preferences > Profiles > General > Show titlebar: off
> -   Preferences > Profiles > Scrolling > Scrollbar is: Disabled

## Files
*   `config` - file that contains gruvbox themes (dark & light) for terminator terminal

## Usage
Install `config` as new configuration file for the terminiator terminal:

```shell
$ mkdir -p ~/.config/terminator/ && wget -O ~/.config/terminator/config https://raw.githubusercontent.com/egel/terminator-gruvbox/master/config
```

Then you can modify your current configuration

```shell
$ vi ~/.config/terminator/config
```

To replace **the default scheme** used for new windows/tabs to gruvbox-dark (or gruvbox-light):

```ini
[[default]]
  # gruvbox-dark theme
  background_color = "#282828"
  cursor_color = "#7c6f64"
  foreground_color = "#ebdbb2"
  palette = "#181818:#cc241d:#98971a:#d79921:#458588:#b16286:#689d6a:#a89984:#928374:#fb4934:#b8bb26:#fabd2f:#83a598:#d3869b:#8ec07c:#ebdbb2"
```

To:

```ini
[[default]]
  # gruvbox-light theme
  background_color = "#eee8d5"
  cursor_color = "#002b36"
  foreground_color = "#002b36"
  palette = "#073642:#dc322f:#859900:#b58900:#268bd2:#d33682:#2aa198:#eee8d5:#002b36:#cb4b16:#586e75:#657b83:#839496:#6c71c4:#93a1a1:#fdf6e3"
```

To configure **the default scheme** used upon launch; change `profile` to your new theme:

```ini
[[default]]
  [[[child1]]]
    type = Terminal
    parent = window0
    profile = default
```

To:

```ini
[[default]]
  [[[child1]]]
    type = Terminal
    parent = window0
    profile = gruvbox-light
```

