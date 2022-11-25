---
title: Install from Source
---

## Mac OS X

This requires homebrew to be installed.

Install dependencies

```
brew update
brew install qt taglib poppler qtkeychain rust
brew link qt --force
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
qmake
make -j$(sysctl -n hw.logicalcpu)
```

## General

TODO: Format

```
pip install cget
cget init --shared
cget install -G "MinGW Makefiles" --release -DCMAKE_C_FLAGS="-fno-asynchronous-unwind-tables"
```

Build dependencies:
* cmake
* yasm
* pkgconfig (lite)

GM-Companion depends on the following libraries:

* Qt >= 5.9
* taglib
* poppler-qt
* wkhtmltopdf
* cmark-gfm
* librespot
* qt5keychain
* openssl