# workspace
The `workspace` command lets you switch to a different workspace.

`workspace next` focuses the numerically greater workspace after the currently
focused one. `workspace prev` focuses in the opposite direction.
`workspace next_on_output` and `workspace prev_on_output` does the same thing
as the previous two commands, but instead the focus list is confined to those
on the focused output.

`workspace back_and_forth` focuses the previously focused workspace.

`workspace [--no-auto-back-and-forth] <name>` focuses a workspace by name.

`workspace [--no-auto-back-and-forth] number <name>` focuses a workspace by name
and number.

## Syntax
```sh
workspace next|prev|next_on_output|prev_on_output
workspace back_and_forth
workspace [--no-auto-back-and-forth] <name>
workspace [--no-auto-back-and-forth] number <name>
```

## Example
```sh
miraclemsg workspace 1     # Focus workspace 1
miraclemsg workspace next  # Focus workspace after 1 (e.g. if workspace 3 exists, 3 would be focused)
miraclemsg workspace hi    # Focus non-numeric workspace named "hi"
```
