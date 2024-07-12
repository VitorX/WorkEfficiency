# Procdump
## [Usage1] Collect second channce crash dump 
    procdump -ma -e <pid|Processname>

# Windbg

## [Usage1] Use shell command to search the output of debug commnand

    .shell -ci "!us" findstr /i "tcp"