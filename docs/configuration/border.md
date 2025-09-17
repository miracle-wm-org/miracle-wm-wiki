# Border
Specify a border for non-focused and focused tiles.

## Key
```
border
```

## Value
```yaml
border:
  size: int  # Size in pixels
  color: Color # Hex color (rgba) or rgba YAML object
  focus_color: Color # Hex color (rgba) or rgba YAML object
  radius: int # Radius in pixels
```

## Example
```yaml
# ~/.config/miracle-wm/config.yaml

border:
  size: 2
  color: 0xffff0000
  focus_color:
    r: 0
    g: 255
    b: 0
    a: 255
  radius: 16
```
