# Introduction
On top of being able to configure miracle with a configuration, miracle also
opens a socket that any client can listen on and send requessts to. This socket
is largely in line with [i3's ipc support](https://i3wm.org/docs/ipc.html),
with additional support for commands provided by [sway's ipc]
(https://github.com/swaywm/sway/blob/master/sway/sway-ipc.7.scd).
In the future, miracle will extend this communication channel for its own purposes.

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
