# Drag and Drop
"Drag and drop" refers to functionality that enables users to drag containers
within or between a tiling grid. If enabled, the user may hold down the modifier
keys and the primary mouse button to begin dragging. The user then moves their
pointer above other containers to drag the active container into that position.
If the user releases the pointer, the container will snap to the desired
location.

## Key
```
drag_and_drop
```

## Value
```yaml
# When set to false, drag and drop is disabled entirely
enabled: boolean

# List of modifiers expected to be held when left clicking.
# Defaults to the primary action key
modifiers: String[]
```

For a list of valid modifiers, see [Action Key](action_key.md).

## Default
```yaml
drag_and_drop:
  enabled: true
  modifiers:
    - primary
    - shift
```

## Example
```yaml
# ~/.config/miracle-wm.yaml

drag_and_drop:
  enabled: true
  modifiers:
    - primary
    - alt
```
