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

```
git clone --recursive https://github.com/IDMIL/MapperUGen.git
cd MapperUGen
mkdir -p build
cmake -B ./build -DSUPERNOVA=ON
cmake --build build --target install
```
