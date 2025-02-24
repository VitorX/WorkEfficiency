# CL.exe 
    Microsoft (R) C/C++ Optimizing Compiler Version 19.42.34438 for x64
    Copyright (C) Microsoft Corporation.  All rights reserved.

## Build dll and lib with /LD
    cl /LD Myputs.cpp

## Link a lib
    cl loadtimecall.cpp /link Myputs.lib

## Link multiple options

    cl WinSDKVer_Button.cpp stdafx.cpp /D UNICODE /link /subsystem:windows WinSDKVer_Button.res user32.lib
## Add unicode support
    cl main.cpp /D UNICODE /D _UNICODE

## set stack size with /stack:reserve[,commit], below sample set the 8k(2000) reserved stack bytes
    cl WinSDKVer_Button.cpp stdafx.cpp /D UNICODE /link /subsystem:windows WinSDKVer_Button.res user32.lib /stack:8192
