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

```
$ gn gen out/Debug
$ ninja -C out/Debug
```

The outputs will be found in `out/Debug/` directory.

### 3. Links

- [GN project homepage](https://gn.googlesource.com/gn)
- [GN Quick Start guide](https://chromium.googlesource.com/chromium/src/tools/gn/+/48062805e19b4697c5fbd926dc649c78b6aaa138/docs/quick_start.md)
- [GN Language and Operation](https://chromium.googlesource.com/chromium/src/tools/gn/+/48062805e19b4697c5fbd926dc649c78b6aaa138/docs/language.md)

### 4. Contact

Email：lujun.hust@gmail.com









