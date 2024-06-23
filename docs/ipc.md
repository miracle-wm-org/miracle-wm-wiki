# IPC Support
Miracle implements [i3's ipc support](https://i3wm.org/docs/ipc.html). In the future, miracle will extend this communication channel for its own purposes.

## i3 IPC Support
The following provides the list of requests that are fully supported:

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

### `RUN_COMMAND` Support
i3 supports a [list of commands](https://i3wm.org/docs/userguide.html#list_of_commands).

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
- ❌ `exit`
- ❌ `scratchpad`
- ❌ `nop`
- ❌ `bar`
- ❌ `gaps`
