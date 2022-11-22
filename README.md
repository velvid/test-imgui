# ImGUI Test

## Overview

This is a mockup project to learn proper environment configuration for an ImGUI application.

## Build steps

### Install vcpkg
```bash
cd /path/to/install/to # i.e "~/dev/"
git clone https://github.com/Microsoft/vcpkg.git
cd vcpkg
export VCPKG_DIR=$(pwd)
```

### Configure and build
```bash
cd /path/to/this/repo
cmake -B ./build -S . "-DCMAKE_TOOLCHAIN_FILE=$VCPKG_DIR/scripts/buildsystems/vcpkg.cmake"
cmake --build ./build
```