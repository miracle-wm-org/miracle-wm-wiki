# Introduction
Miracle provides an IPC mechanism for interacting with the compositor at runtime.
This socket is largely in line with both [i3](https://i3wm.org/docs/ipc.html) and 
[sway]((https://github.com/swaywm/sway/blob/master/sway/sway-ipc.7.scd))'s IPC implementation.

 The IPC protocol uses a UNIX socket as the method of communication. The path to the socket
 is stored in the environment variable `MIRACLESOCK`  and, for backwards compatibility with sway, SWAYSOCK,
 and, for backwards compatibility with i3, I3SOCK.

## Format
The format for messages and replies is:

```
    <magic-string> <payload-length> <payload-type> <payload>

Where
    <magic-string> is i3-ipc, for compatibility with i3
    <payload-length> is a 32-bit integer in native byte order
    <payload-type> is a 32-bit integer in native byte order
```

For example, sending the exit command would look like the following hexdump:

```
00000000 | 69 33 2d 69 70 63 04 00 00 00 00 00 00 00 65 78 |i3-ipc........ex|
00000010 | 69 74                                           |it              |
```

The payload for replies will be a valid serialized JSON data structure.

## Messages
Each message is associated with a "Message Type" that is given by the number in parentheses. This is
the value that users will send from the client when they want to send the corresponding message.

- [RUN_COMMAND (0)](run_command.md)
- [GET_WORKSPACES (1)](get_workspaces.md)
- [SUBSCRIBE (2)](subscribe.md)
- [GET_OUTPUTS (3)](get_outputs.md)
- [GET_TREE (4)](get_tree.md)
- [GET_MARKS (5)](get_marks.md)
- [GET_VERSION (7)](get_version.md)
- [GET_BINDING_MODES (8)](get_binding_modes.md)
- [SEND_TICK (10)](send_tick.md)
- [SYNC (11)](sync.md)
- [GET_BINDING_STATE (12)](get_binding_state.md)

For those familiar with sway, miracle will always lack support for particular messages
such as:

- `GET_CONFIG`
- `GET_BAR_CONFIG`

The following are unimplemented, but may be implemented in the future:

- `GET_INPUTS`
- `GET_SEATS`

## Events
- [tick (0x80000007)](./events/tick.md)
- [window (0x80000003)](./events/window.md)

## Commands
- [layout](./commands/layout.md)
- [mark](./commands/mark.md)
- [resize](./commands/resize.md)
- [swap](./commands/swap.md)
- [sticky](./commands/sticky.md)
- [workspace](./commands/workspace.md)
- [rename](./commands/rename.md)

## Messages
The following provides the list of requests that are supported:

- ✅ `RUN_COMMAND`
- ✅ `GET_WORKSPACES`
- 🔨 `SUBSCRIBE`
- ✅ `GET_OUTPUTS`
- 🔨 `GET_TREE`
- ❌ `GET_BAR_CONFIG`
- ❌ `GET_MARKS`
- ✅ `GET_VERSION`
- ✅ `GET_BINDING_NODES`
- ❌ `SEND_TICK`
- ❌ `SYNC`
- ✅ `GET_BINDING_STATE`


## Supported commands:
i3 and sway support a [list of commands](https://i3wm.org/docs/userguide.html#list_of_commands).

The following provides a list of **criteria** queries that are supported:

- ✅ `all`
- ❌ `class`
- ❌ `instance`
- ❌ `window_role`
- ❌ `window_type`
- ❌ `machine`
- ❌ `id`
- ✅ `title`
- ❌ `urgent`
- ❌ `workspace`
- ❌ `con_mark`
- ❌ `con_id`
- ❌ `floating`
- ❌ `floating_from`
- ❌ `tiling`
- ❌ `tiling_from`

The following provides a list of **commands** that are supported:

- ✅ `exec`
- ✅ `split`
- ❌ `layout`
- ✅ `focus`
- ✅ `move`
- ❌ `swap`
- ✅ `sticky`
- ❌ `workspace`
- ❌ `move` containers or windows to a different screen
- ❌ `move` containers or windows to a mark
- ❌ `resize`
- ❌ `mark`
- ❌ `unmark`
- ❌ `title_format`
- ❌ `title_window_icon`
- ❌ `border`
- ❌ `shmlog`
- ❌ `debuglog`
- ❌ `restart`
- ❌ `reload`
- ✅ `exit`
- ❌ `scratchpad`
- ❌ `nop`
- ❌ `bar`
- ❌ `gaps`
