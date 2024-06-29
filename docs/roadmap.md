# Roadmap
The goal is to have an environment that I am comfortable daily-driving by **July 2024**.
This goal will be marked by the `1.0.0` release. Until then, all releases will be
`0.x.0`.

The dates attached to these releases aren't set in stone. Any release may come
earlier if the work is done. Also, new features may be added to the release while it's
in progress if priority changes, which may push back the release date.


## ✅ 0.1.0
**Proof of Concept (Due: February 17th)**

Features:

- [x] Window management
    * [x] Layout of new windows
    * [x] Delete window
    * [x] Resizing windows
    * [x] Gaps in windows
    * [x] Account for minimum sizes on windows (e.g. gedit)
    * [x] Handle exclusion zones
    * [x] Handle fullscreen windows
- [x] Navigation
    * [x] Changing selected window with keyboard
    * [x] Moving window with keyboard shortcuts
- [x] Outputs
    * [x] Output creation
    * [x] Output updating
    * [x] output deletion
- [x] Application quit command
- [x] Workspaces
    * [x] Workspace switching
    * [x] Moving windows between workspaces
- [x] Configuration
    * [x] Gap size
    * [x] Action key
    * [x] Startup apps
    * [x] Startup apps
    * [x] Override default keybindings
    * [x] Custom keybindings

## ✅ 0.2.0
**Stabilization + Usability (Due: April 15th)**

Features:

- [x] Major bugs + performance
    * [x] No crashes after a week of daily-driving
- [x] Configuration
    * [x] Hot reloading
    * [x] Resize jump
    * [x] Outer gaps
- [x] Floating windows
    * [x] Floating window support (pop out of/into tiles, resizing, moving)
    * [x] "Pin to workspace" mode
- [x] I3 IPC support for workspaces
- [x] Packaging
    * [x] Deb (jammy, mantic, noble, multi-architecture)
    * [x] Fedora


## 🚧 0.3.0
**Aimations + Sway IPC Release (Due: June 15th)**

This release relies on having the *Mir*'s renderer capabilities opened up to us.
If we can override the renderer, we can put *whatever we like* on the screen.

Features:

- [x] Highlight border around selected window (carry over from **0.2.0**)
- [x] Animation (requires access to Mir renderer)
    * [x] Window movement interpolation
    * [x] Window size interpolation
    * [x] Workspace change
    * [x] Move window to workspace
    * [x] Opening
    * [x] Configuration support
- [x] Multi monitor support
    * [x] Zero monitors

## 0.4.0
**Pointer Support + Animation + More I3 IPC (Due August 30th)**

Features:

- [ ] Stacking windows
- [ ] Support for i3 containers
- [ ] Pointer support for tiling actions
    - [ ] Drag tiles around
    - [ ] Resize tiles with pointer
- [ ] Animation
    - [ ] Closing windows
- [ ] Configuration
    * [ ] Display configuration (depends on https://github.com/mattkae/miracle-wm/issues/93)
- [ ] Full I3 IPC integration
- [ ] Increase test coverage using thew new harness

## 1.0.0
**Official Release (Due October 15th)**

Features:

- [ ] Bug free
- [ ] Tons of test coverage
- [ ] **IDEA**: Workspace/window overview view (similar to GNOME)
- [ ] **IDEA**: Settings app
- [ ] **IDEA**: Context menu on window with support for actions
- [ ] **IDEA**: Focus mode, where the focused application appears up front and center
- [ ] **IDEA**: A minimal default shell, including a panel, launcher, background, etc.
- [ ] **IDEA**: "Freestyle tiling": This would mean that tiling can extend beyond the screen and that the screen can be navigated via scrolling, panning, or anchor points. Workspaces would still be available in this mode, although they would be less relevant.
- [ ] **IDEA**: Workspaces could be unified in one mega scrolling view to give the illusion of one continuous workspace with "sections"
