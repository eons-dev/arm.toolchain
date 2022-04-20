# ARM gnueabihf Toolchain

Intended host: 64 bit Linux (img_generic-builder)
Intended target: Currently popular embedded boards, like Raspberry Pi 3B+ and Raspberry Pi 4 (Linux)

cmake file inspired by: https://kubasejdak.com/how-to-cross-compile-for-embedded-with-cmake-like-a-champ

## Compilers

GCC retrieved from: https://developer.arm.com/tools-and-software/open-source-software/developer-tools/gnu-toolchain/gnu-rm/downloads

## How To Use

Use this toolchain with `ebbs . -b cpp --toolchain arm`.
Please refer to the [ebbs documentation](https://github.com/eons-dev/bin_ebbs) for more info.

NOTE: `CMAKE_C_FLAGS` includes `-mcpu=cortex-a53 -mfpu=neon-vfpv4 -mfloat-abi=hard` which should work for Raspberry Pi 3, hopefully 4. This may be generalized to include other boards in a future release.

For more on cross compiling for the Raspberry Pi, check out: https://github.com/Pro/raspi-toolchain/blob/master/Toolchain-rpi.cmake