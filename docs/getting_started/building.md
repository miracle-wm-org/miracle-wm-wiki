# Building

## Dependencies
- [cmake](https://cmake.org/) >= 3.7
- [gcc](https://gcc.gnu.org/) or [clang](https://clang.llvm.org/) with C++23 support
- [miral](https://canonical-mir.readthedocs-hosted.com/stable/tutorial/) >= 7
- [mirrenderer](https://canonical-mir.readthedocs-hosted.com/stable/tutorial/)
- [mirwayland](https://canonical-mir.readthedocs-hosted.com/stable/tutorial/)
- [mirserver](https://canonical-mir.readthedocs-hosted.com/stable/tutorial/)
- [mirserver-internal](https://canonical-mir.readthedocs-hosted.com/stable/tutorial/)
- [mir-graphics-drivers-desktop](https://canonical-mir.readthedocs-hosted.com/stable/tutorial/) >= 2.14
- [mir-graphics-drivers-nvidia](https://canonical-mir.readthedocs-hosted.com/stable/tutorial/) >= 2.14 (NVIDIA Only)
- [glib-2.0](https://docs.gtk.org/glib/)
- [yaml-cpp](https://github.com/jbeder/yaml-cpp)
- [libevdev](https://www.freedesktop.org/wiki/Software/libevdev/)
- [nlohmann json](https://github.com/nlohmann/json) >= 3.2.0
- [libnotify](https://gitlab.gnome.org/GNOME/libnotify)
- [libxkbcommon](https://github.com/xkbcommon/libxkbcommon)
- [libgles2-mesa-dev](https://docs.mesa3d.org/opengles.html)
- [json-c](https://github.com/json-c/json-c) >= 0.17


## From source
```sh
git clone https://github.com/miracle-window-manager/miracle-wm.git
cd miracle-wm

cmake -Bbuild
cmake --build build
WAYLAND_DISPLAY=wayland-98 ./build/miracle-wm
```

### CMake Options
The following options are available at build time:

- `-DSNAP_BUILD`: Informs cmake that this is being built for a snap
  since some parameters need to be tweaked for that use case.
- `-DSYSTEMD_INTEGRATION`: If enabled, miracle will build with full
  systemd integration, including establishing a user session and
  importing the proper environment variables in to systemd.


## Snap
```sh
cd miracle-wm
snapcraft
sudo snap install --dangerous --classic miracle-wm_*.snap
```
