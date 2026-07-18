# Haikoo

A Haiku OS–style window decoration plugin for KDE Plasma 6 with the help of Besot theme..

![Inspired by HaikuOS and Besot Haiku theme for the Plasma](https://www.opencode.net/phob1an/besot/)

<img width="1053" height="768" alt="preview" src="https://github.com/user-attachments/assets/11eac63e-e8e9-499b-a2ba-0bc63c01b4d5" />


## Features

- **Content-fit tab** — the yellow title bar tab grows/shrinks to fit its buttons and title text, not a percentage of window width
- **SVG-based graphics** — tab gradients and bevels rendered from the original Haiku OS decoration SVGs
- **Pre-rendered button states** — close, minimize, maximize, and restore buttons with hover/pressed states for both active and inactive windows
- **Transparent titlebar** — the area to the right of the tab is transparent, showing your desktop wallpaper
- **No visible borders** — clean edge-to-edge look with invisible resize handles

## Dependencies

- CMake 3.16+
- Qt 6.6+ (Core, Gui, Widgets)
- KDE Frameworks 6.2+ (CoreAddons, ConfigWidgets, WidgetsAddons)
- KDecoration3

### Installing dependencies

**Ubuntu/Debian:**
```bash
sudo apt install cmake extra-cmake-modules qt6-base-dev \
  libkf6configwidgets-dev libkf6widgetsaddons-dev libkdecorations3-dev
```

**Fedora:**
```bash
sudo dnf install cmake extra-cmake-modules qt6-base-devel \
  kf6-kconfigwidgets-devel kf6-kwidgetsaddons-devel kdecorations-devel
```

**Arch Linux:**
```bash
sudo pacman -S cmake extra-cmake-modules qt6-base kf6-configwidgets kf6-widgetsaddons libkdecorations2
```

## Building

```bash
git clone https://github.com/your-username/haikoo.git
cd haikoo
cmake -B build -DCMAKE_INSTALL_PREFIX=/usr
cmake --build build
```

## Installing

```bash
sudo cmake --install build
```

Then open **System Settings → Window Management → Window Decorations**, find **Haiku** in the list, and click **Apply**.

## Uninstalling

```bash
sudo rm /usr/lib/qt6/plugins/org.kde.kdecoration3/haikoo.so \
        /usr/lib/qt6/plugins/org.kde.kdecoration3/deco.json
```

## Credits

- Window decoration and button images based on [besot by phob1an](https://www.opencode.net/phob1an/besot)
- Original Haiku OS design by [Haiku, Inc.](https://www.haiku-os.org/)

## License

[GPL-2.0](LICENSE)
