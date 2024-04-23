# Outer Gaps
Gaps between the window tiles and the edge of the screen.

## Key
```
outer_gaps
```

## Value
A 2D integer point describing the gaps in pixels in the X and Y directions:
```yaml
x: int
y: int
```

## Default
```yaml
x: 10
y: 10
```

## Example
```yaml
# ~/.config/miracle-wm.yaml

outer_gaps:
    x: 50  # 50px between the tiling grid and the edge of the output, horizontally
    y: 100 # 100px between the tiling grid and the edge of the output, vertically 
```
