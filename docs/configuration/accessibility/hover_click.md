# Hover Click
Hover Click is an accesibility feature that enables users to click by simply
hovering their cursor over a position for a period of time. This is useful for
users who find it hard to move the pointer and click at the same time.

## Key
```
hover_click
```

## Value
```yaml
# Whether the feature is enabled or not
enabled: boolean

# The duration in miliseconds before a click is issued.
#
# Defaults to 1000 milliseconds.
hover_duration: uint

# The pointer displacement in pixels required to cancel a pending click.
# This is useful for users who struggle to hold the pointer in one position
# without shaking it.
#
# Defaults to 10 pixels.
cancel_displacement_threshold: int

# The pointer displacement in pixels that the pointer needs to move after
# a click in order for a new click to be issued.
#
# Defaults to 5 pixels.
reclick_displacement_threshold: int
```

## Example
```yaml
# ~/.config/miracle-wm/config.yaml

hover_click:
    enable: true
    hover_duration: 5000
    cancel_displacement_threshold: 50
    reclick_displacement_threshold: 5
```
