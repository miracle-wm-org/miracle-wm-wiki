# Includes
The **includes** options provides a way to compose configuration files. This
is useful in cases when you want to share or distribute some base configuration
across many machines, but each machine needs some unique override to make
things work correctly. For example, it may be more useful to bind `alt` as the
action key on a laptop and `meta` as the action key on a desktop.

Files are loaded in the order in which they are provided in the list. If a path
is invalid, the file is skipped and not loaded. Files loaded later have priority
over files loaded earlier, meaning that the "included" file may potentially
override values set in the parent file. Configuration values that are lsits
will be concatenated, with "included" files being concatenated at the front
of the list in order to gain priority.

## Key
```
includes
```

## Value
A list of strings, each of which is a path. The path may start with `~` to
specify the user's home directory.

```yaml
string[]
```

## Default
An empty list.

## Example
```yaml
# ~/.config/miracle-wm/config.yaml

includes:
    - ~/.config/miracle-wm/user_config.yaml
    - ~/.config/miracle-wm/colors.yaml
```
