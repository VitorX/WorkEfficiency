# JSON
JQ command for windows

## Install
    pacman -S mingw-w64-x86_64-jq
## Add to Windows enviroment 
By default jq.exe is installed in 'C:\msys64\usr\bin', add this path to the Windows enviroment system variables Path.

### List Edge Policies
>jq ".policyValues.chrome.policies|keys" samplePolicies

![alt text](.\images\image.png)

### Show Edge policy 
>jq ".policyValues.chrome.policies.HomepageLocation" samplePolicies.json

![alt text](.\images\image-1.png)

