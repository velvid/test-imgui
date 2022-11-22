# ImGUI Test

## Overview

This is a mockup project to learn proper environment configuration for an ImGUI application.

## Build steps

### Install vcpkg
```sh
cd /path/to/install/to # i.e "~/dev/"
git clone https://github.com/Microsoft/vcpkg.git
cd vcpkg
export PATH=$PATH:$(pwd)
```

### Configure and build
```
cd /path/to/this/repo
cmake -B ./build -S . "-DCMAKE_TOOLCHAIN_FILE=$VCPKG_DIR/scripts/buildsystems/vcpkg.cmake"
cmake --build ./build
```