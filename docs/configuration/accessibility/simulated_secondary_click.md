# Simulated Secondary Click
Simulated secondary click enables the user to issue a right-click by holding
down the left mouse button for some duration of time.

## Key
```
simulated_secondary_click
```

## Value
```yaml
# Whether simulated secondary click is enabled or not
enabled: boolean

# The duration in milliseconds that the left button must be held before a
# right-click is issued.
hold_duration: uint

# A displacement in pixels that the pointer is allowed to move by while
# holding the left mouse buttion before the right-click is cancelled
displacement_threshold: int
```

## Example
```yaml
# ~/.config/miracle-wm/config.yaml

simulated_secondary_click:
    enable: true
    hold_duration: 5000
    displacement_threshold: 50
```

