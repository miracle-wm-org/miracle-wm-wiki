# Building

## Dependencies
- [cmake](https://cmake.org/) >= 3.7
- [gcc](https://gcc.gnu.org/) or [clang](https://clang.llvm.org/) with C++20 support
- [miral](https://canonical-mir.readthedocs-hosted.com/stable/getting_and_using_mir/) >= 6
- [mir-graphics-drivers-desktop](https://canonical-mir.readthedocs-hosted.com/stable/getting_and_using_mir/) >= 2.14
- [mir-graphics-drivers-nvidia](https://canonical-mir.readthedocs-hosted.com/stable/getting_and_using_mir/) >= 2.14 (NVIDIA Only)
- [glib-2.0](https://docs.gtk.org/glib/)
- [yaml-cpp](https://github.com/jbeder/yaml-cpp)
- [libevdev](https://www.freedesktop.org/wiki/Software/libevdev/)
- [nlohmann json](https://github.com/nlohmann/json) >= 3.2.0
- [libnotify](https://gitlab.gnome.org/GNOME/libnotify)
- [libxkbcommon-devel](https://github.com/xkbcommon/libxkbcommon)


## From source
```sh
git clone https://github.com/mattkae/miracle-wm.git
cd miracle-wm

cmake -Bbuild
cmake --build build
WAYLAND_DISPLAY=wayland-98 ./build/bin/miracle-wm
```

## Snap
```sh
cd miracle-wm
snapcraft
sudo snap install --dangerous --classic miracle-wm_*.snap
```
