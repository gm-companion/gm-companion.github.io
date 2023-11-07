---
title: Install from Source
---

If you are unsure about a step have a look at the [CI config](https://github.com/PhilInTheGaps/GM-Companion/tree/master/.github/workflows)
and if you still need help, feel free to start a discussion on [GitHub](https://github.com/PhilInTheGaps/GM-Companion/discussions).

## Prerequisites

The following tools/libraries need to be installed.

### Build Tools

* [CMake](https://cmake.org/) >= 3.26
* A modern C++ compiler with c++17 support ([g++](https://gcc.gnu.org/), [Clang](https://clang.llvm.org/) and [MSVC](https://visualstudio.microsoft.com/de/vs/features/cplusplus/) have been tested)

### Libraries

The application depends on a few libraries which can either be installed through a package manager or compiled from source:

* [Qt](https://www.qt.io/) >= 6.5
* [QtKeychain](https://github.com/frankosterfeld/qtkeychain)
* [TagLib](https://taglib.org/)
* [Poppler-Qt](https://gitlab.freedesktop.org/poppler/poppler/)
* One of the following markdown libraries:
  * [cmark-gfm](https://github.com/github/cmark-gfm)
  * [discount](https://github.com/Orc/discount)
* [Quazip](https://github.com/stachenov/quazip)

### Optional

Optionally [librespot](https://github.com/librespot-org/librespot) is required if you want to play music from Spotify.

## Build

Download the source code using git:

```sh
git clone https://github.com/philinthegaps/gm-companion
cd gm-companion
git submodule update --init --recursive
```

Create a build directory:

```sh
mkdir build
cd build
```

Run cmake:

```sh
cmake .. -D CMAKE_INSTALL_PREFIX=install -D CMAKE_BUILD_TYPE=Release
cmake --build . --config Release --parallel
cmake --install . --config Release
```

Run `install/bin/gm-companion`.