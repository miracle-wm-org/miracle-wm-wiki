# Cursor
Describes the cursor configuration.

## Key
```
cursor
```

## Value
```yaml
# The scale of the cursor.
#
# Defaults to 1.
scale: float

# How to focus windows with the cursor.
#
# Defaults to "hover".
focus_mode: hover, click
```

## Example
```yaml
# ~/.config/miracle-wm/config.yaml

cursor:
    scale: 4.0 # Sets the cursor scale to 4 times its original size.
    focus_mode: click # Click a mouse button while hovering a window to focus
```
