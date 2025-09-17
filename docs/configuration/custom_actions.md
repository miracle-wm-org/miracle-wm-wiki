# Custom Actions
The user may define a list of **custom actions**, which are shell commands
bound to a specific key combination. These actions always have preference
over those defined in [Default Keybinds](#default_keybinds.md) when they are
bound to the same key combination.

## Key
```
custom_actions
```

## Value
A list of: 

```yaml
# The shell command that you want to execute
- command: string

# The key action that will trigger the default action
 - action: "up" | "down" | "repeat" | "modifiers"

# A list of modifiers that need to accompany the action for the command to happen
- modifiers: Modifier[]

# Name of the keycode that the action should respond to.
# See https://github.com/torvalds/linux/blob/master/include/uapi/linux/input-event-codes.h
# for the list of available keycodes (e.g. KEY_ENTER, KEY_Z, etc.)
- key: KeyCodeName
```

A `Modifier` is defined as one of the following names:

| Name | Description |
| ---- | ----------- |
| `primary` | the key defined by the [Action Key](action_key.md) |
| `alt` | Any alt key |
| `alt_left` | The left alt key only |
| `alt_right` | The right alt key only |
| `shift` | Any shift key |
| `shift_left` | The left shift key only |
| `shift_right` | The right shift key only |
| `ctrl` | Any ctrl key |
| `ctrl_left` | The left ctrl key only |
| `ctrl_right` | The right ctrl key only |
| `meta` | The `super` or `windows` key |
| `meta_left` | The left `super` or `windows` key only |
| `meta_right` | The right `super` or `windows` key only |
| `sym` | The sym key |
| `function` | The `fn` key |
| `caps_lock` | The caps lock key |
| `num_lock` | The num lock key |
| `scroll_lock` | The scroll lock key |

## Example
```yaml
# ~/.config/miracle-wm/config.yaml

custom_actions:           # Set meta + D to open wofi
  - command: wofi --show=drun
    action: down
    modifiers:
      - primary
    key: KEY_D
```
