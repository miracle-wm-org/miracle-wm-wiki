# Touchpad
Describes the touchpad configuration

## Key
```
touchpad
```

## Value
```yaml
# Whether or not the touchpad is disabled while typing.
#
# Defaults to false.
disable_while_typing: boolean

# Whether or not to disable the touchpad when an external mouse
# is connected.
#
# Defaults to false.
disable_with_external_mouse: boolean

# The acceleration bias of the touchpad.
#
# This is a number between [-1, 1].
#
# Defaults to 0.
acceleration_bias: float

# The vertical scroll speed of the touchpad.
#
# Defaults to 1.
vscroll_speed: float

# The horizontal scroll speed of the touchpad.
#
# Defaults to 1.
hscroll_speed: float

# Whether tap-to-click is enabled.
#
# Defaults to true.
tap_to_click: boolean

# Whether middle mouse button emulation is enabled.
#
# Defaults to false.
middle_mouse_button_emulation: boolean

# The click mode for the touchpad.
#
# Defaults to none.
click_mode: none | area_to_click | finger_count 

# The scroll mode for the touchpad.
#
# Defaults to two_finger_scroll.
scroll_mode: none | two_finger_scroll | edge_scroll | button_down_scroll
```

## Example
```yaml
touchpad:
    disable_while_typing: true
    tap_to_click: true
    middle_mouse_button_emulation: true
    vscroll_speed: 1.2
    acceleration_bias: -0.1
    click_mode: none
    scroll_mode: two_finger_scroll
```
