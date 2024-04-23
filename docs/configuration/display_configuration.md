# Display Configuration

> Please note that the display configuration **is distinct from the configuration defined in
> the [configuration section](file.md). The two may indeed overlap with one another. There is a task
> in miracle-wm to [fix this](https://github.com/mattkae/miracle-wm/issues/93).


The [Mir](https://github.com/canonical/mir) project provides a mechanism for configuring
the display in a reproducible way. To use this, you may provide the following commandline
argument when running miracle:

```
--display-config=static=/path/to/a/display/file.yaml
```

Alternatively, you may define the `display-config` option in [Mir's Built-in Configuration](mir.md), e.g.:

```
# ~/.config/miracle-wm.config

display-config=static=/path/to/a/display/file.yaml
```
