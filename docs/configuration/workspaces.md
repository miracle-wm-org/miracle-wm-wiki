# Workspaces
Customize the behavior of a particular workspace number.

## Key
```
workspaces
```

## Value
A list of:

```yaml
number: int  # Unique que of the workspace [0-9]
layout: tiled, floating  # Default layout style for this workspace
```

## Default
```yaml
workspaces:
    - number: 0
      layout: tiled
    - number: 1
      layout: tiled
    - number: 2
      layout: tiled
    - number: 3
      layout: tiled
    - number: 4
      layout: tiled
    - number: 5
      layout: tiled
    - number: 6
      layout: tiled
    - number: 7
      layout: tiled
    - number: 8
      layout: tiled
    - number: 9
      layout: tiled
```

## Example
```yaml
# ~/.config/miracle-wm.yaml

workspaces:
    - number: 1
      layout: floating  # Override the default layout style to floating
```
