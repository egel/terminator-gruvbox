# Terminator gruvbox colors

A color theme for [terminator](http://www.tenshu.net/terminator/) using Pavel Pertsev’s [Gruvbox color scheme](https://github.com/morhetz/gruvbox).

## Screenshots
![gruvbox terminator](http://i.imgur.com/HjSy0Ga.png)

## Files
*   `config` - gruvbox theme for terminator terminal

## Usage
Install the terminiator configuration file:

```shell
$ mkdir -p ~/.config/terminator/
$ cp config ~/.config/terminator/
```

Modify the defaults stanza within the terminator configuration file to select your default(s)

```shell
$ vi ~/.config/terminator/config
```

To configure the default scheme used for new windows/tabs to gruvbox-light; change:

```ini
[[default]]
# gruvbox-dark
background_color = "#282828"
cursor_color = "#7c6f64"
foreground_color = "#ebdbb2"
palette = "#181818:#cc241d:#98971a:#d79921:#458588:#b16286:#689d6a:#a89984:#928374:#fb4934:#b8bb26:#fabd2f:#83a598:#d3869b:#8ec07c:#ebdbb2"
```

To:

```ini
[[default]]
# gruvbox-light
background_color = "#eee8d5"
cursor_color = "#002b36"
foreground_color = "#002b36"
palette = "#073642:#dc322f:#859900:#b58900:#268bd2:#d33682:#2aa198:#eee8d5:#002b36:#cb4b16:#586e75:#657b83:#839496:#6c71c4:#93a1a1:#fdf6e3"
```

To configure the default scheme used upon launch; change:

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

