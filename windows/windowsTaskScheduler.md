# Add Startup task to Windows 

## Open Windows command to specific path when startup
    schtasks /Create /tn "FreeRTOS" /tr "C:\Windows\System32\cmd.exe /k cd C:\Users\v-feixue1\Documents\dev\FreeRTOS & title RTOS" /SC ONSTART