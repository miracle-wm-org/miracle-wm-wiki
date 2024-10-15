# Layout

Introduced in v0.4.0, the `layout` command allows users to to change the layout
of the currently selected container.

## Example
```sh
miraclemsg command "layout splitv"  # Set the layout to 'vertical'
miraclemsg command "layout splith"  # Set the layout to 'horizontal'
miraclemsg command "layout toggle split"  # Set the layout to 'vertical' if 'horizontal' and vice versa
miraclemsg command "layout toggle tabbed splith splitv"  # Cycle through the layouts in the list
```

## Links
- [i3 documentation](https://i3wm.org/docs/userguide.html#manipulating_layout)