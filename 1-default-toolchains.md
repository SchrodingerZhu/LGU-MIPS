# 1 Default Toolchains [lgu-mips.dtc]

## 1.1 MUSL Libc [lgu-mips.dtc.musl]

The course use `musl-libc` with static compilation as the default toolchain. 

MUSL libc project have already packaged a statically linked GCC environment. 
The quickest way to setup a compiler for MIPS(el) is to download it from MUSL's website [musl.cc](https://musl.cc). 
The package to use is [mipsel-linux-musl-cross.tgz](https://musl.cc/mipsel-linux-musl-cross.tgz).  
(For those who favor in docker images rather than native packages, MUSL also offers an option; please refer to the website if needed.)

The files are installed into `/mipsel-linux-musl-cross`.
Basic executables are soft linked into `/usr/bin/` with the following command:
```bash
ln -s /mipsel-linux-musl-cross/bin/mipsel-linux-musl-cc /usr/bin/mcc   
ln -s /mipsel-linux-musl-cross/bin/mipsel-linux-musl-gcc /usr/bin/mgcc 
ln -s /mipsel-linux-musl-cross/bin/mipsel-linux-musl-g++ /usr/bin/mg++ 
ln -s /mipsel-linux-musl-cross/bin/mipsel-linux-musl-c++ /usr/bin/mc++ 
ln -s /mipsel-linux-musl-cross/bin/mipsel-linux-musl-nm /usr/bin/mnm   
ln -s /mipsel-linux-musl-cross/bin/mipsel-linux-musl-objdump /usr/bin/mobjdump
```


## 1.2 Arch Linux [lgu-mips.dtc.os]

The grading environment is set to follow latest Arch Linux and additional packages from `archlinuxcn`, distributed at the beginning of every term. Some of the essential components are listed below:

- GCC
- Cmake
- Ninja
- iverilog
- qemu-headless
- qemu-arch-extra

Normally, `Dockerfile` and Virtualbox/VMWare OVA files are provided.

## 1.3 GDB Multiarch [lgu-mips.dtc.debugger]

For `CSC3050`, the images should have include a debugger named `gdb-multiarch`. It can be compiled from `aur/gdb-multiarch`.

## 1.4 Mars [lgu-mips.dtc.mars]

While for `CSC4180`, the code generation target is Linux ELF; for `CSC4050`, we use MARS Simulator. 

## 1.5 Auxiliary Materials [lgu-mips.dtc.aux]

Together with this chapter, there are auxiliary materials, talking about how to compile, execute and debug the assembly files
