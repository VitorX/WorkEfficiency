# Search Text from URL
Required Packge: w3m
## Install
    pacman -S w3m

## [Usage1]Search [coplilot] key words from Edge policy page

    w3m -dump https://learn.microsoft.com/en-us/deployedge/microsoft-edge-policies|grep --color=always -i copilot
## [Usage2]Search group policy name about [coplilot] key words from Edge policy page
    w3m -dump https://learn.microsoft.com/en-us/deployedge/microsoft-edge-policies|grep -i copilot|grep --color=always -i gp

