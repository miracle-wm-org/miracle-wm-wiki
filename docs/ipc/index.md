# IPC
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
- [RUN_COMMAND](run_command.md)
- [GET_WORKSPACES](get_workspaces.md)
- [SUBSCRIBE](subscribe.md)

## Messages
The following provides the list of requests that are supported:

- ✅ `RUN_COMMAND`
- ✅ `GET_WORKSPACES`
- 🔨 `SUBSCRIBE`
- ✅ `GET_OUTPUTS`
- 🔨 `GET_TREE`
- ❌ `GET_BAR_CONFIG`
- ✅ `GET_VERSION`
- ✅ `GET_BINDING_NODES`
- ❌ `GET_CONFIG`
- ❌ `SEND_TICK`
- ❌ `SYNC`
- ✅ `GET_BINDING_STATE`

## Commands
- [Layout](./commands/layout_command.md)

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
