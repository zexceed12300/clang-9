## LLVM Clang-9 & GCC-4.9 from googlesource

### Set up Environtment Variables
This is very important. set up clang to source

#### For AArch64 target
```
export ARCH=arm64
export PATH="/path/to/clang-9/bin:/path/to/clang-9/aarch64-linux-android-4.9/bin:/path/to/clang-9/arm-linux-androideabi-4.9/bin:${PATH}"
export CLANG_TRIPLE=aarch64-linux-android-
export CROSS_COMPILE=aarch64-linux-android-
export CROSS_COMPILE_ARM32=arm-linux-androideabi-
```
#### For ARM target
```
export ARCH=arm
export PATH="/path/to/clang-9/bin:/path/to/clang-9/arm-linux-androideabi-4.9/bin:${PATH}"
export CLANG_TRIPLE=arm-linux-androideabi-
export CROSS_COMPILE=arm-linux-androideabi-
export CROSS_COMPILE_ARM32=arm-linux-androideabi-
```

### HowTo compile kernel with clang?
Add CC=clang argument on make command. example:
```
make -j$(nproc) CC=clang
```
