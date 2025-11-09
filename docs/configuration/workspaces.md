# Workspaces
Customize the behavior of a particular workspace number.

## Key
```
workspaces
```

## Value
A list of:

```yaml
# The number of the workspace.
#
# Either name, number, or both must be provided.
number: int?

# The name of the workspace.
#
# Either name, number, or both must be provided.
name: string?

# The default layout strategy for the workspace.
#
# New windows will be placed either in the tiling grid or floating in their
# own tree by default.
layout: tiling, floating
```

## Default
```yaml
workspaces:
    - number: 0
      layout: tiling
    - number: 1
      layout: tiling
    - number: 2
      layout: tiling
    - number: 3
      layout: tiling
    - number: 4
      layout: tiling
    - number: 5
      layout: tiling
    - number: 6
      layout: tiling
    - number: 7
      layout: tiling
    - number: 8
      layout: tiling
    - number: 9
      layout: tiling
```

## Example
```yaml
# ~/.config/miracle-wm/config.yaml

# Override workspace 1's layout strategy such that all new windows are floating.
workspaces:
    - number: 1
      layout: floating
```
