---
title: Linux
weight: 1
---

[![Packaging status](https://repology.org/badge/vertical-allrepos/gm-companion.svg)](https://repology.org/project/gm-companion/versions)

## AppImage

[Download 64-bit](https://github.com/PhilInTheGaps/GM-Companion/releases/download/1.1.0/gm-companion-1.1.0_amd64.AppImage)  
The AppImage is built using Ubuntu 16.04 LTS.

You might have to install `gstreamer 1.0` otherwise audio cannot be played. For me this version works on Ubuntu but not on Manjaro.

## Arch Linux

Install from [AUR](https://aur.archlinux.org/packages/gm-companion/):

```
yay -S gm-companion
```

## Ubuntu

Currently your best option is to build from source:  
(I am working on a ppa)

### Ubuntu 18.10

```
git clone --recursive https://github.com/PhilInTheGaps/GM-Companion

sudo apt-get install qtbase5-dev qt5-default qttools5-dev qtmultimedia5-dev libqt5opengl5-dev libqt5x11extras5-dev libqt5xmlpatterns5-dev qtdeclarative5-dev libqt5network5 libqt5webengine5 libqt5webenginecore5 libqt5networkauth5-dev libqt5core5a libqt5multimedia5 libqt5multimedia5-plugins libqt5network5 libqt5networkauth5 libqt5opengl5 libqt5script5 libqt5widgets5 libqt5xml5 libqt5xmlpatterns5 libqt5gui5 libqt5qml5 libqt5quick5 qml-module-qtquick-layouts qml-module-qtquick-window2 libqt5quickcontrols2-5 qml-module-qtquick2 qml-module-qtquick-controls libqt5webengine5 libqt5webenginecore5 libqt5multimediaquick5 libqt5quickwidgets5 libpoppler-qt5-dev

cd GM-Companion
qmake
make
```
run: `./gm-companion`  
or install:
```
make install
gm-companion
```

### Ubuntu 18.04

```
git clone --recursive https://github.com/PhilInTheGaps/GM-Companion

sudo add-apt-repository ppa:beineri/opt-qt-5.12.1-bionic
sudo apt-get update
sudo apt-get install binutils libpulse-dev qt512base qt512declarative qt512graphicaleffects qt512imageformats qt512multimedia qt512networkauth-no-lgpl qt512quickcontrols qt512quickcontrols2 qt512script qt512tools qt512translations qt512webengine libegl1-mesa-dev libglu1-mesa-dev mesa-utils libpoppler-qt5-dev

source /opt/qt512/bin/qt512-env.sh

cd GM-Companion
qmake
make
```
run: `./gm-companion`  
or install:
```
make install
gm-companion
```

### Ubuntu 16.04

```
git clone --recursive https://github.com/PhilInTheGaps/GM-Companion

sudo add-apt-repository ppa:beineri/opt-qt-5.12.1-xenial
sudo apt-get update
sudo apt-get install binutils libpulse-dev qt512base qt512declarative qt512graphicaleffects qt512imageformats qt512multimedia qt512networkauth-no-lgpl qt512quickcontrols qt512quickcontrols2 qt512script qt512tools qt512translations qt512webengine libegl1-mesa-dev libglu1-mesa-dev mesa-utils libpoppler-qt5-dev

source /opt/qt512/bin/qt512-env.sh

cd GM-Companion
qmake
make
```
run: `./gm-companion`  
or install:
```
make install
gm-companion
```

## Debian

(Debian Buster)

Install build dependencies

```
sudo apt install build-essential qt5-default libqt5network5 libqt5networkauth5-dev libqt5quick5 qtdeclarative5-dev qtmultimedia5-dev qtquickcontrols2-5-dev libpoppler-qt5-dev qt5keychain-dev libtag1-dev openssl qml-module-qt-labs-folderlistmodel qml-module-qt-labs-platform qml-module-qt-labs-settings qml-module-qtquick-controls2 qml-module-qtquick-controls qml-module-qtquick-dialogs qml-module-qtquick-extras qml-module-qtquick-window2 qml-module-qtquick2 cargo libasound2-dev -y
```

Get librespot

```
cargo install librespot
```

Get source code

```
git clone https://github.com/philinthegaps/gm-companion
cd gm-companion
git submodule update --init --recursive
```

Build GM-Companion

```
qmake CONFIG+=release PREFIX=/usr
make -j$(nproc)
```

## Arch / Manjaro

Install dependencies

```
sudo pacman -S base-devel
```

// TODO

## Fedora

Install dependencies

```
sudo dnf groupinstall "Development Tools"
sudo dnf install qt5 qt5-devel poppler-qt5-devel qtkeychain-devel taglib-devel
```

Get source code

```
git clone https://github.com/philinthegaps/gm-companion
cd gm-companion
git submodule update --init --recursive
```

Create workaround links for qtkeychain

```
sudo ln -s /usr/include/qtkeychain /usr/include/qt5keychain
sudo ln -s /usr/lib64/libqtkeychain.so /usr/lib64/libqt5keychain.so
```

Build GM-Companion

```
qmake-qt5 CONFIG+=release PREFIX=/usr
make -j$(nproc)
```

## Other Distros

1. `git clone --recursive https://github.com/PhilInTheGaps/GM-Companion`
2. Install [Qt5](https://www.qt.io/) >=5.10  
3. Install [Poppler-Qt5](https://poppler.freedesktop.org/)  
4. Build the program:
```
cd GM-Companion
qmake
make
```
run: `./gm-companion`  
or install:
```
make install
gm-companion
```
