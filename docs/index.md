# miracle-wm

## About
miracle-wm is a Wayland compositor based on [Mir](https://github.com/MirServer/mir). It features a tiling window manager at its core, very much in the style of [i3](https://i3wm.org/) and [sway](https://github.com/swaywm/sway). The intention is to build a compositor that is flashier and more feature-rich than either of those compositors, like [swayfx](https://github.com/WillPower3309/swayfx).

See the [installation guide](getting_started/installation.md) for installation instructions on your platform.

## Features
- A tiling window manager, similar to `i3` and `sway`
    - Built-in support for inner/outer gaps
- An optional floating window manager for individual windows
- A [YAML configuration file](./configuration/file.md)
- Support for the following wayland protocols:
    - ext_session_lock_manager_v1
    - mir_shell_v1
    - wl_shell
    - xdg_wm_base
    - zwlr_foreign_toplevel_manager_v1
    - zwlr_layer_shell_v1
    - zwlr_screencopy_manager_v1
    - zwlr_virtual_pointer_manager_v1
    - zwp_input_method_manager_v2
    - zwp_text_input_manager_v1
    - zwp_text_input_manager_v2
    - zwp_text_input_manager_v3
    - zwp_virtual_keyboard_manager_v1
    - zxdg_output_manager_v1
    - zxdg_shell_v6
    - zwp_idle_inhibit_manager_v1
    - zwp_input_method_v1
    - zwp_input_panel_v1
    - zwp_pointer_constraints_v1
    - zwp_primary_selection_device_manager_v1
    - zwp_relative_pointer_manager_v1
- Support for a wide array of graphics cards, including hybrid systems and outputs driven by Nvidia's proprietary drivers
- Workspace support
- Growing support for `i3`/`sway` IPC
    - A minimal implementation for `waybar` at the moment



## Links
- [Github Repository](https://github.com/mattkae/miracle-wm)
- [Snapcraft.io listing](https://snapcraft.io/miracle-wm)
- [Mir](https://github.com/canonical/mir), the library that `miracle-wm` uses for all of the heavy-lifting
- [Miriway](https://github.com/Miriway/Miriway), another compositor built on top of *Mir*
