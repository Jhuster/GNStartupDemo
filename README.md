# GNStartupDemo

Startup demo for GN/Ninja build system.

### 1. Install build environment

##### 1.1 Build & Install GN

```shell
$ git clone https://gn.googlesource.com/gn
$ cd gn
$ python build/gen.py
$ ninja -C out
```

The standalone gn tools will located in `gn/out` directory. Please add the path to your $PATH env.

##### 1.2 Install Ninja

```shell
$ git clone https://chromium.googlesource.com/chromium/tools/depot_tools.git
```

The Ninja tools will located in depot_tools directory. Please add the path to your $PATH env.

### 2. Build demos

```shell
$ gn gen out/Debug
$ ninja -C out/Debug
```

The outputs will be found in `out/Debug/` directory.

### 3. Overall build flow

- Look for .gn file in the current directory and walk up the directory tree until one is found. Set this directory to be the “source root” and interpret this file to find the name of the build config file.
- Execute the build config file (The name of this file is specified in the .gn file that marks the root of the repository, this is the default toolchain).
- Load the BUILD.gn file in the root directory.
- Recursively load BUILD.gn in other directories to resolve all current dependencies. If a BUILD file isn't found in the specified location, GN will look in the corresponding location inside tools/gn/secondary.
- When a target's dependencies are resolved, write out the .ninja file to disk.
- When all targets are resolved, write out the root build.ninja file.


### 4. Links

- [GN project homepage](https://gn.googlesource.com/gn)
- [GN Quick Start guide](https://chromium.googlesource.com/chromium/src/tools/gn/+/48062805e19b4697c5fbd926dc649c78b6aaa138/docs/quick_start.md)
- [GN Language and Operation](https://chromium.googlesource.com/chromium/src/tools/gn/+/48062805e19b4697c5fbd926dc649c78b6aaa138/docs/language.md)

### 5. Contact

Email：lujun.hust@gmail.com









