# Sticky Keys
Sticky keys is an accessibility feature that enables users to type a keyboard
shortcut one key at a time instead of having to hold down all modifier keys at
once. For example, a user who wants to move the focused window to workspace
two could click `Super` then `Shift` and finally `2` in order to move the window.

## Key
```
sticky_keys
```

## Value
```yaml
# Whether or not sticky keys is enabled.
#
# Defaults to `false`.
enabled: boolean

# When set to true, depressing two modifier keys simultaneously will
# result in sticky keys being temporarily disabled until all keys are
# released.
#
# Defaults to `true`
should_disable_if_two_keys_are_pressed_together: boolean
```

## Example
```yaml
# ~/.config/miracle-wm/config.yaml

sticky_keys:
    enabled: true
    should_disable_if_two_keys_are_pressed_together: false
```