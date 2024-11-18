# miracle-wm

miracle-wm is a Wayland compositor based on
[Mir](https://github.com/MirServer/mir). It features a tiling window manager at
its core, very much in the style of [i3](https://i3wm.org/) and
[sway](https://github.com/swaywm/sway). Miracle provides an experience that is flashier and more feature-rich than either of those compositors, like [swayfx](https://github.com/WillPower3309/swayfx).

See the [installation guide](getting_started/installation.md) for installation instructions on your platform.

## Features
- Support for manual tiling window management
- Support for floating window management
- Driven by a [YAML configuration file](./configuration/introduction.md)
- Support for many common wayland protocols which you can see on [Wayland Explorer](https://wayland.app/protocols/)
- Support for a wide array of graphics cards, including hybrid systems and outputs driven by Nvidia's proprietary drivers
- Workspace support
- Support for [i3 ipc](https://i3wm.org/docs/ipc.html)
- Animation support
- Window bordering
- etc.

## Links
- [Github Repository](https://github.com/miracle-wm-org/miracle-wm)
- [Trello Board](https://trello.com/b/ldzWTZDK/miracle)
- [Snapcraft.io listing](https://snapcraft.io/miracle-wm)
- [Fedora Miracle Spin](https://fedoraproject.org/spins/miraclewm/)
- [Mir](https://github.com/canonical/mir), the library that `miracle-wm` uses for all of the heavy-lifting
- [Miriway](https://github.com/Miriway/Miriway), another compositor built on top of *Mir*

!!! note
    If none of this makes any sense to you or you're new to Wayland or Linux, check out the [What is a Wayland compositor?](getting_started/what_is_a_wayland_compositor.md) document for a structured walk through the entire ecosystem.
