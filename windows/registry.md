# Network Proxy Config
## Enable proxy by PC level
    reg add  "HKLM\SOFTWARE\Policies\Microsoft\Windows\CurrentVersion\Internet Settings" /v ProxySettingsPerUser /t REG_DWORD /d 0 /f
    reg add  "HKLM\Software\Microsoft\Windows\CurrentVersion\Internet Settings" /v AutoDetect /t REG_DWORD /d 1 /f
    reg add  "HKLM\Software\Microsoft\Windows\CurrentVersion\Internet Settings" /v AutoConfigURL /t REG_SZ /d "https://test/my_proxy.pac" /f
    reg add "HKLM\Software\Microsoft\Windows\CurrentVersion\Internet Settings" /v ProxyEnable /t REG_DWORD /d 1 /f
    reg add "HKLM\Software\Microsoft\Windows\CurrentVersion\Internet Settings" /v ProxyServer /t REG_SZ  /d "ProxyServer:9999" /f
    reg add "HKLM\Software\Microsoft\Windows\CurrentVersion\Internet Settings" /v ProxyOverride /t REG_SZ /f

## Disable proxy by PC level
    reg delete  "HKLM\SOFTWARE\Policies\Microsoft\Windows\CurrentVersion\Internet Settings" /v ProxySettingsPerUser  /f
    reg delete "HKLM\Software\Microsoft\Windows\CurrentVersion\Internet Settings" /v AutoDetect  /f
    reg delete "HKLM\Software\Microsoft\Windows\CurrentVersion\Internet Settings" /v AutoConfigURL  /f
    reg delete "HKLM\Software\Microsoft\Windows\CurrentVersion\Internet Settings" /v ProxyEnable  /f
    reg delete "HKLM\Software\Microsoft\Windows\CurrentVersion\Internet Settings" /v ProxyServer  /f
    reg delete "HKLM\Software\Microsoft\Windows\CurrentVersion\Internet Settings" /v ProxyOverride  /f

## Query Proxy by PC level 

    reg query "HKLM\SOFTWARE\Policies\Microsoft\Windows\CurrentVersion\Internet Settings" /v ProxySettingsPerUser  
    reg query "HKLM\Software\Microsoft\Windows\CurrentVersion\Internet Settings" /v AutoDetect  
    reg query "HKLM\Software\Microsoft\Windows\CurrentVersion\Internet Settings" /v AutoConfigURL  
    reg query "HKLM\Software\Microsoft\Windows\CurrentVersion\Internet Settings" /v ProxyEnable  
    reg query "HKLM\Software\Microsoft\Windows\CurrentVersion\Internet Settings" /v ProxyServer  
    reg query "HKLM\Software\Microsoft\Windows\CurrentVersion\Internet Settings" /v ProxyOverride  

## Enable Proxy by user level
    reg add  "HKLM\SOFTWARE\Policies\Microsoft\Windows\CurrentVersion\Internet Settings" /v ProxySettingsPerUser /t REG_DWORD /d 1 /f
    reg add "HKCU\Software\Microsoft\Windows\CurrentVersion\Internet Settings" /v AutoDetect /t REG_DWORD /d 1 /f
    reg add "HKCU\Software\Microsoft\Windows\CurrentVersion\Internet Settings" /v AutoConfigURL /t REG_SZ /d "https://test/my_proxy.pac" /f
    reg add "HKCU\Software\Microsoft\Windows\CurrentVersion\Internet Settings" /v ProxyEnable /t REG_DWORD /d 1 /f
    reg add "HKCU\Software\Microsoft\Windows\CurrentVersion\Internet Settings" /v ProxyServer /t REG_SZ  /d "ProxyServer:9999" /f
    reg add "HKCU\Software\Microsoft\Windows\CurrentVersion\Internet Settings" /v ProxyOverride /t REG_SZ /f
## Disable Proxy by user level
    reg delete  "HKLM\SOFTWARE\Policies\Microsoft\Windows\CurrentVersion\Internet Settings" /v ProxySettingsPerUser  /f
    reg delete "HKLM\Software\Microsoft\Windows\CurrentVersion\Internet Settings" /v AutoDetect  /f
    reg delete "HKLM\Software\Microsoft\Windows\CurrentVersion\Internet Settings" /v AutoConfigURL  /f
    reg delete "HKLM\Software\Microsoft\Windows\CurrentVersion\Internet Settings" /v ProxyEnable  /f
    reg delete "HKLM\Software\Microsoft\Windows\CurrentVersion\Internet Settings" /v ProxyServer  /f
    reg delete "HKCU\Software\Microsoft\Windows\CurrentVersion\Internet Settings" /v ProxyOverride  /f

## Query Proxy by user level 

    reg query  "HKCU\SOFTWARE\Policies\Microsoft\Windows\CurrentVersion\Internet Settings" /v ProxySettingsPerUser  
    reg query "HKCU\Software\Microsoft\Windows\CurrentVersion\Internet Settings" /v AutoDetect  
    reg query "HKCU\Software\Microsoft\Windows\CurrentVersion\Internet Settings" /v AutoConfigURL  
    reg query "HKCU\Software\Microsoft\Windows\CurrentVersion\Internet Settings" /v ProxyEnable  
    reg query "HKCU\Software\Microsoft\Windows\CurrentVersion\Internet Settings" /v ProxyServer  
    reg query "HKCU\Software\Microsoft\Windows\CurrentVersion\Internet Settings" /v ProxyOverride  

# Reg Query for a speicifc key
    reg query "HKLM\Software\Microsoft\Windows\CurrentVersion\Internet Settings"  /v /f *
