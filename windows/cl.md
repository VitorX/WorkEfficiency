# CL.exe 
    Microsoft (R) C/C++ Optimizing Compiler Version 19.42.34438 for x64
    Copyright (C) Microsoft Corporation.  All rights reserved.

## Build dll and lib with /LD
cl /LD Myputs.cpp

## Link a lib
cl loadtimecall.cpp /link Myputs.lib
