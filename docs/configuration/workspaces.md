# Workspaces
Customize the behavior of a particular workspace number.

## Example
```yaml
# ~/.config/miracle-wm/config.yaml

# Override workspace 1's layout strategy such that all new windows are floating.
workspaces:
    - number: 1
      layout: floating
```

## Schema

A list of workspace configurations:

```yaml
workspaces:
  - number?: <int>
    name?: <string>
    layout: <tiling|floating>
```

## Properties

### `number`

:   **type:** Integer

    The number of the workspace. Either `name`, `number`, or both must be provided.

### `name`

:   **type:** String

    The name of the workspace. Either `name`, `number`, or both must be provided.

### `layout`

:   <small>required</small> **type:** `tiling` | `floating`

    The default layout strategy for the workspace:
    
    - `tiling` — New windows will be placed in the tiling grid by default
    - `floating` — New windows will float in their own tree by default

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
