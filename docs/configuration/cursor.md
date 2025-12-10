# Cursor
Describes the cursor configuration.

## Example
```yaml
# ~/.config/miracle-wm/config.yaml

cursor:
    scale: 4.0 # Sets the cursor scale to 4 times its original size.
    focus_mode: click # Click a mouse button while hovering a window to focus
```

## Schema

```yaml
cursor:
  scale?: <float>
  focus_mode?: <hover|click>
```

## Properties

### `scale`

:   **type:** Float  
    **Default:** `1.0`

    The scale multiplier of the cursor. A value of `2.0` makes the cursor twice its original size.

### `focus_mode`

:   **type:** `hover` | `click`  
    **Default:** `hover`

    How to focus windows with the cursor:
    
    - `hover` — Focus windows by hovering over them with the cursor
    - `click` — Click a mouse button while hovering a window to focus it

## Default
```yaml
cursor:
  scale: 1.0
  focus_mode: hover
```
