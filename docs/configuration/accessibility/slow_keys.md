# Slow Keys
The slow keys accessibility feature allows users to insert a delay between the
time that a key is pressed and the time that it is propagated to clients.

## Key
```
slow_keys
```

## Value
```yaml
# Whether or not slow keys is enabled.
#
# Defaults to false.
enabled: boolean

# The time in milliseconds between key down and key propagation.
#
# Defaults to 200 milliseconds.
hold_delay: uint
```

## Example
```yaml
# ~/.config/miracle-wm/config.yaml

slow_keys:
    enabled: true
    hold_delay: 5000  # 5 seconds, which is an outrageously large delay
```