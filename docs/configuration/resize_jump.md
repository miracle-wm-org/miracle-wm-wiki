# Resize Jump
Defines the number of pixels that a window will be resized by for each resize request.
This value affects any direction (up, down, left, or right).

## Key
```
resize_jump
```

## Value
An integer describing the number of pixels

## Default
```
50
```

## Example
```yaml
# ~/.config/miracle-wm.yaml

resize_jump: 25 # Each resize will now add or remove 25px from the current window size
```
