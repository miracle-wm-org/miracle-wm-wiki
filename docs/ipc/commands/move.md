# move
Finalized in v0.7.0, the `move` command allows users to move
containers and workspaces in a variety of ways.

## syntax
```sh
move window|container to mark <mark>  # Moves the container/window to the mark provided by <mark>, if any exists
move workspace to output left|right|down|up|current|primary|nonprimary|next|<output1> [output2]…  # Moves the active workspace to another output
```

## Example
```sh
move container to mark meow     # Moves the focused container to mark "meow"
move workspace to output right  # Moves the current workspace to the output directly to the right of the active output
```

## Links
- [i3 documentation for "move ... to mark"](https://i3wm.org/docs/userguide.html#move_to_mark)
- [i3 documentation for "move workspace"](https://i3wm.org/docs/userguide.html#_moving_workspaces_to_a_different_screen)
