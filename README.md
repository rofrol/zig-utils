# Zig Scripts

A collection of utility scripts I use for zig

## Important

These scripts need a `zig` folder to exist in `$HOME/.local` as well as this containing
a `ver` folder, with a temporary folder in it called whatever your heart desires, and you must
then create a symlink to it in the `zig` folder so that your directory structure looks like this:

```txt
$HOME/.local/zig
  |- ver
      |- temp
  |- current (symlink to ver/temp)
```

## zupd-src

The `zupd-src` script is an updater script that builds from source. In order for this script to work you'll also
need the [necessary dependencies](https://github.com/ziglang/zig/wiki/Building-Zig-From-Source#dependencies) to build zig.

After everything here has been setup correctly, you can use it by running for example:

```bash
zupd-src x86_64-linux-gnu
```

After it finishes building, the finished compiler is in `$HOME/.local/zig/current` so make sure it's in your path.

## zupd

The `zupd` script, similar to `zupd-src` is an updater script, however this script pulls from the repository rather than building from source.
This option is usually better for beginners as you only really need simple dependencies such as `curl`, `jq`, `tar` and other common linux utilities.

To use this script, you simply need to run it with the platform you want to install for:

```bash
zupd x86_64-linux
```
