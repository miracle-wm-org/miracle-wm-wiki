# Mouse Configuration
Configure the mouse input device.

## Key
```
mouse
```

## Value
```yaml
# The handedness of the mouse.
#
# Setting this will change which button is considered 'primary'.
# Defaults to "right".
handedness: "left" | "right"

# The verical scroll speed, if supported.
#
# Defaults to 1.
vscroll_speed: double

# The horizontal scroll speed if supported.
#
# Defaults to 1. 
hscroll_speed: double

# The acceleration bias of your mouse.
#
# Between [-1, 1]. A value of -1 will be slow, and a value of
# 1 will be fast. Defaults to 0.
acceleration_bias: double

# The acceleration type of your mouse.
#
# Defaults to "none".
acceleration: "none" | "adaptive"
```

## Example
```yaml
# ~/.config/miracle-wm.yaml

# Override the mouse configuration to change the handedness to left
# and slow down the pointer speed
mouse:
    handedness: left
    acceleration_bias: -0.5
```
