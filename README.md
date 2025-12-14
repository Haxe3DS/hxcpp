# hxcpp (Nintendo Switch support)

This fork of hxcpp has all the modifications needed to compile Haxe for the Nintendo Switch.
[Code taken from an old fork of hxcpp for the Nintendo Switch](https://github.com/retronx-team/switch-hxcpp) along with more changes in some parts of hxcpp to achieve a successful compilation for the console.

To use this, check out [HaxeNXCompiler](https://github.com/Slushi-Github/HaxeNXCompiler).

**Please note that not everything provided by HXCPP has been tested on this experimental target.**

## Current problems
- Socket (``src/hx/libs/std/Socket.cpp``) is not supported (due to issues with MBEDTLS), so you can't use ``sys.net.Socket``.

- CFFI requires an implementation for this target.

- There appears to be a problem when the program ends that prevents it from releasing all the memory correctly, causing a crash.

-----

### Minor Changes
- You can define ``HXCPP_SL_DETAIL_NULL_REF`` to obtain information about the object that was referenced null. 