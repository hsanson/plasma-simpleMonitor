Simple Monitor for Plasma
=========================

A simple monitor for plasma, completely written in QML and Javascript.

Dependencies
============

- Plasma 5 (Plasma Shell) (better use Plasma >= 5.10 with plasmoid autoresize fix)

### Extra Dependencies For CMake ###

Only needed if you use `cmake` to install this widget.

- CMake >= 3.16.3
- Extra CMake Modules (`extra-cmake-modules`)
- Plasma Framework Development Package (`libkf5plasma-dev`)

Installation
============

### CMake ###

If you need localisation (i18n/l10n) support, please use `cmake` to install this widget to your system-wide directory. You also would need root permission.

````Shell
git clone https://github.com/dhabyx/plasma-simpleMonitor.git plasma-simpleMonitor
cd plasma-simpleMonitor
mkdir build
cd build
cmake -DCMAKE_INSTALL_PREFIX=$(kf5-config --prefix) -DCMAKE_BUILD_TYPE=Release  -DKDE_INSTALL_USE_QT_SYS_PATHS=ON ../
sudo make install
````
### Plasma PKG ###

This way may be more convenient, but localisation support is not possible via `plasmapkg2`. This widget will be installed into your home directory.

Replace the version number as needed.

Installing from .plasmoid file:
````Shell
plasmapkg2 -i plasma-simpleMonitor-0.6.plasmoid
````
For upgrade, run `plasmapkg2 -u plasma-simpleMonitor-0.6.plasmoid` instead.

Installing from sources:
````Shell
git clone https://github.com/dhabyx/plasma-simpleMonitor.git plasma-simpleMonitor
cd plasma-simpleMonitor/plasmoid
plasmapkg2 -t plasmoid -i ./plasmoid
````
For upgrade, run `plasmapkg2 -t plasmoid -u ./plasmoid` instead.

Packaging
=========

Simple way for make plasmoid package:

````Shell
git clone https://github.com/dhabyx/plasma-simpleMonitor.git plasma-simpleMonitor
cd plasma-simpleMonitor/plasmoid
zip -r plasma-simpleMonitor.plasmoid contents metadata.desktop
````

Development
===========

Use launch.sh script to launch and debug plasma-simpleMonitor plasmoid without install it.
Use clearLaunch.sh script to clean sources from files generated by launch.sh.

If you love QtCreator IDE visit the [wiki](https://github.com/dhabyx/plasma-simpleMonitor/wiki) for more details.

License
=======
Simple Monitor for Plasma is licensed under the GNU General Public License Version 3 or later.

You can modify or/and distribute it under the conditions of this license.
