---
title: Windows
weight: 2
---

[Release 1.1.0 (Win x64)](https://github.com/PhilInTheGaps/GM-Companion/releases/download/1.1.0/gm-companion_1.1.0_win64.zip)  

The program works without an installer. Simply extract all the files from the .zip archive to a folder and run _gm-companion.exe_.

## Build from Source

### Requirements

- [Qt](https://www.qt.io/download)
  - install the latest LTS version
- [MinGW](http://mingw.org/)
  - can be installed through the Qt installer
- [TagLib](https://taglib.org/)
  - [pre-compiled binaries](https://github.com/PhilInTheGaps/taglib-bin/releases)
- [Poppler](https://poppler.freedesktop.org/)
  - [pre-compiled binaries](https://github.com/PhilInTheGaps/poppler-bin/releases)
- [qtkeychain](https://github.com/frankosterfeld/qtkeychain)
  - [pre-compiled binaries](https://github.com/PhilInTheGaps/qtkeychain-bin/releases)
- (optional) [librespot](https://github.com/librespot-org/librespot)
  - if you intent to use Spotify
  - [pre-compiled binaries](https://github.com/PhilInTheGaps/librespot-bin/releases)

### Build Instructions

Get source code

```
git clone https://github.com/philinthegaps/gm-companion
cd gm-companion
git submodule update --init --recursive
```

Unpack build dependencies

- unpack poppler.zip to gm-companion\lib\poppler
- unpack qt5keychain.zip to gm-companion\lib\qt**5**keychain
- unpack taglib.zip to gm-companion\lib\taglib

Build

```
qmake DEFINES-=NO_UPDATE_CHECK CONFIG+=qtquickcompiler CONFIG+=release PREFIX=install
mingw32-make -j%NUMBER_OF_PROCESSORS%
mingw32-make check
mingw32-make install
```

Fetch libraries

```
cd src\install\bin
set QT_PATH=<e.g C:\Qt\5.12.8\mingw73_64>
windeployqt.exe -xml --release --qmldir %QT_PATH%\qml gm-companion.exe
```

Copy additional libraries

- copy contents of the bin directories from taglib.zip, poppler.zip and qt5keychain.zip to src\install\bin
- if you intent to use Spotify, copy librespot.exe to src\install\bin
  - make sure the file is named librespot.exe and not librespot-x86_64.exe
  - alternatively if you installed librespot from cargo make sure the cargo bin directory is in your path