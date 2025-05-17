# Display Configuration

The display configuration is a distinct YAML file from the regular configuration.
It is populated on the initial startup of `miracle` with a basic information for
your particular monitor sitation if it does not yet exist.

The most likely location is:

```
~/.config/miracle-wm/display.yaml.
```

!!! note
    See the [arch user guide](https://wiki.archlinux.org/title/XDG_Base_Directory) for information about `$XDG_CONFIG_HOME`.

You may specify an alternative location by providing the commandline argument:

```sh
miracle-wm --display-config-path=/path/to/file
```

## Configuration
The contents of the file describe a list of outputs. If the output is in the list, it is
considered "used" and will have the provided attributes applied to it. An output is
matched by its `name`. All attributes aside from the `name` are optional.

```yaml
  outputs:
    name: string      # the name of the output to match
    enabled: boolean  # whether or not the output is used
    primary: boolean  # whether or not the output is primary. If set true on multiple outputs, only the first one will be primary.
    position:         # the XY position of the output
      x: int
      y: int
    size:             # the size of the output, must match a resolution that the output supports, otherwise ignored
      width: int
      height: int
    refresh: double   # the refresh rate of the output, must match a valid resolution that the output supports, otherwise ignored
    orientation: normal | inverted | left | right
    scale: float      # a scale factor for the whole output
    group_id: int     # when non-zero, outputs with the same group_id will display the same content
```

## Example
The following example is similar to something that might populate the default configuration. It tells the
displays to be displayed side-by-side with their own content at normal orientations.

```yaml
# ~/.config/miracle-wm/display.yaml 
outputs:
  - enabled: true
    name: HDMI-A-1
    position:
      x: 0
      y: 0
    size:
      width: 1920
      height: 1290
    refresh: 60
    orientation: normal
    scale: 1
    group_id: 0
  - enabled: true
    name: HDMI-A-2
    position:
      x: 1280
      y: 0
    size:
      width: 800
      height: 600
    refresh: 60
    orientation: normal
    scale: 1
    group_id: 0
```
