# Windbg

##  Use shell command to search the output of debug commnand

    .shell -ci "!us" findstr /i "tcp"

##  Use NETEXT dump socket info
    !wsocket
## Set breakpoint for load specific dll
    sxe ld Something.dll

Refer to [netext](https://github.com/rodneyviana/netext) extension for more.
