# ImGUI Test Project

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

### For VSCode users

To automatically configure, add this in  `.vscode/settings.json`:

```json
{
    "cmake.configureOnOpen": false,
    "cmake.configureSettings": {
        "CMAKE_TOOLCHAIN_FILE": "$VCPKG_DIR/vcpkg/scripts/buildsystems/vcpkg.cmake"
    }
}
```

This should allow you to build and run through VSCode.