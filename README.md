# Zig Scripts

A collection of utility scripts I use for zig

## zupd-src

The `zupd-src` script is an updater script that builds from source. In order to use it
you're going to need to have the following dependencies:

* ninja
* cmake
* build-essential (or equivalent)
* llvm-libs
* lld-libs
* clang
* llvm

The script also requires a `zig` folder to exist in `$HOME/.local` as well as this containing
a `ver` folder, with a temporary folder in it called whatever your heart desires, and you must
then create a symlink to it in the `zig` folder so that your directory structure looks like this:

```txt
$HOME/.local/zig
  |- ver
      |- temp
  |- current (symlink to ver/temp)
```

After everything here has been setup correctly, you can use it by running for example:

```bash
zupd-src x86_64-linux-gnu
```
