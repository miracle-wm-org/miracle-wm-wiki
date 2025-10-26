# Magnifier
The magnifier accessibility feature allows users to zoom in on an area of the
desktop centered around their mouse cursor.

See the [Default Keybinds](../default_keybinds.md) sections for the keybindings
associated with the magnifier.

## Key
```
magnifier
```

## Value
```yaml
# Whether or not the magnifier is enabled by default. 
enabled: boolean

# The scale of the magnifier.
#
# Defaults to 1.5.
scale: float

# The scale increment of the magnifier.
#
# When the magnifier is zoomed in or out using the keybinds, this is the increment
# by which that will happen. The magnifier's zoom is clamped to 1 as a minimum.
#
# Defaults to 0.5.
scale_increment: float

# The default width of the magnified area.
#
# Defaults to 400px.
width: int

# The default height of the magnifier area.
#
# Defaults to 400px.
height: int

# The size increment of the magnifier.
#
# When the magnifier's zoomed area increases or decreases in size via the keyboard shortcut,
# this is the increment by which that will happen. The magnifier's size is clamped to 100x100.
#
# Defaults to 50px
size_increment: int
```

## Example
```yaml
# ~/.config/miracle-wm/config.yaml

magnifier:
    enabled: true
    scale: 2
    scale_increment: 0.25
    width: 500
    height: 500
    size_increment: 25
```
