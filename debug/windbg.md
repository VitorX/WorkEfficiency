# Windbg

##  Use shell command to search the output of debug commnand

    .shell -ci "!us" findstr /i "tcp"

##  Use NETEXT dump socket info
    !wsocket

Refer to [netext](https://github.com/rodneyviana/netext) extension for more.