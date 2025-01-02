# Drag and Drop
The **drag and drop** configuration defines how containers can be moved using
the cursor in `miracle-wm`.

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

## Example
```yaml
# ~/.config/miracle-wm.yaml

drag_and_drop:
  enabled: true
  modifiers:
    - primary
    - alt
```
