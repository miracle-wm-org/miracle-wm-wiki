# Default Keybinds
The compositors comes ships with a number of built-in commands. By default, these
commands are bound to preset keybinds, but the user may change them to whatever
they want. These commands may be overridden more than once and will respond to multiple key combinations as a result. Defining at least one override disables the default action.

The default commands defined in the compositor are described in this table:

| Name | Description | Keybind |
| ---- | ----------- | ------- |
| `terminal` | Opens a new terminal | `❖ Super + Enter` |
| `request_vertical` | Requests that the current window layout future windows vertially| `❖ Super + v` |
| `request_horizontal` | Requests that the current window layout future windows horizontaly | `❖ Super + h` |
| `select_up` | Select the window above currently selected window | `❖ Super + ↑` |
| `select_down` | Select the window above currently selected window | `❖ Super + ↓` |
| `select_left` | Select the window above currently selected window | `❖ Super + ←` |
| `select_right` | Select the window above currently selected window | `❖ Super + →` |
| `move_up` | Move the currently selected window upwards | `❖ Super + ⇧ Shift + ↑` |
| `move_down` | Move the currently selected window downwards | `❖ Super + ⇧ Shift + ↓` |
| `move_left` | Move the currently selected window to the left | `❖ Super + ⇧ Shift + ←` |
| `move_right` | Move the currently selected window to the right | `❖ Super + ⇧ Shift + →` |
| `toggle_resize` | Toggle resize mode on the active window | `❖ Super + r` |
| `resize_up` | When resize mode is toggled on, this will decrease the size of the window vertically | `❖ Super + ↑` (only in resize mode)  |
| `resize_down` | When resize mode is toggled on, this will increase the size of the window vertically | `❖ Super + ↓` (only in resize mode) |
| `resize_left` | When resize mode is toggled on, this will decrease the size of the window horizontally | `❖ Super + ←` (only in resize mode)  |
| `resize_down` | When resize mode is toggled on, this will increase the size of the window horizontally | `❖ Super + →` (only in resize mode)  |
| `fullscreen` | Fullscreen the currently selected window | `❖ Super + f` |
| `quit_active_window` | Close the currently selected window | `❖ Super + ⇧ Shift + Q` |
| `quit_compostior` | Exit the compositor | `❖ Super + ⇧ Shift + E` |
| `select_workspace_[0-9]` | Select the workspace between 0-9 | `❖ Super + [0-9]` |
| `select_workspace_[0-9]` | Move the currently selected window to the workspace between 0-9 | `❖ Super + ⇧ Shift + [0-9]` |
| `toggle_floating` | Toggle whether or not the currently selected window is floating | `❖ Super + Space` |
| `toggle_pinned_to_workspace` | Toggle whether a floating window is pinned outside of a workspace or not | `❖ Super + ⇧ Shift + P` |
| `toggle_tabbing` | Toggle whether or not the currently selected container is in a tabbed layout mode | `❖ Super + W` |
| `toggle_stacking` | Toggle whether or not the currently selected container is in a stacking layout mode | `❖ Super + S` |

## Key
```
default_action_overrides
```

## Value
A list of: 

```yaml
# The name of the action that you want to override (taken from the list above)
- name: string

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

default_action_overrides:
  - name: terminal        # Override the "terminal" keybind to execute with "Ctrl + Shift + Enter"
    action: down
    modifiers:
      - ctrl
      - shift
    key: KEY_ENTER
```
