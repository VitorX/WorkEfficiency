# gdb

## ADD the gdb config file on windows via Msys2

Create .gdbinit file on C:\users\{username}. We can also use %userprofile% to identify the directory which we should create the config file.

More config/init file for GDB, refer to the offical link:
[Initialization Files](https://sourceware.org/gdb/download/onlinedocs/gdb.html/Initialization-Files.html).

## Common commands
### Check value via 'x', below command is examine memory at the address of $rax for 10 hex(x) byte(b)
    x/10xb $rax
### Find help for key words
    apropos 'keywolds'
### Show Assembly layout
    layout asm
### Show/Set disassebmly-flavor
    show disassembly-flavor
    set disassembly-flavor intel
### Set breakpoints at main method
    b main
### run the progream
    r
### Add the exe as target program
    target exec a.exe