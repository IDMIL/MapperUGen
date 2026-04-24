# MapperUGen

A SuperCollider UGen for using libmapper

## Prerequisites

### Install libmapper

Please follow the [libmapper](https://github.com/libmapper/libmapper) documentation, unless your configuration is covered by specific cases below:

#### macOS with homebrew

- Install [Homebrew](https://brew.sh/)
- Install dependencies
    ```
    brew install boost libmapper
    ```

## Installation from releases

* Install [SuperCollider](https://supercollider.github.io/)
* Unzip MapperUGen.zip from [releases](https://github.com/IDMIL/MapperUGen/releases) into SuperCollider extensions folder (Platform.userExtensionDir)

## Compilation from source

### GNU/Linux or macOS

```
git clone --recursive https://github.com/IDMIL/MapperUGen.git
cd MapperUGen
mkdir -p build
cmake -B ./build -DSUPERNOVA=ON
cmake --build build --target install
```

### Windows

Note: when cloning supercollider below, if the cloning hangs just execute `git config --global url."https://".insteadOf git://` to fix the issue. It's a known issue with older versions of the supercollider SDK.

```
git clone https://github.com/libmapper/MapperUGen.git
cd MapperUGen
git config --global url."https://".insteadOf git://
git submodule update --init --recursive
```

Now edit the CMakeLists.txt LIBMAPPER_DIR and LIBLO_DIR paths to match with your local libmapper paths. For libmapper installation help, consult the instructions [here](https://github.com/libmapper/libmapper/blob/main/doc/how_to_compile_and_run.md). Finally:

```
mkdir build
cd build
cmake -DSUPERNOVA=ON ..
cmake --build .
```

#### Windows manual installation after compiling

1. Evaluate `Platform.userExtensionDir` in supercollider and create a "Mapper" folder there
2. Copy everything inside the ./sc folder to the Mapper folder
3. Create a "plugins" folder in the Mapper directory
4. Copy the build outputs from ./build/Debug and your libmapper, liblo and zlib .dlls to the plugins folder
5. Reboot the supercollider interpreter