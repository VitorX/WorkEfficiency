# Search Process/Service via wmic

## Filter the Servcie on Windows
    wmic process where caption="svchost.exe" get csname,name,caption,commandline,processid

## Filter the msedge.exe process and exclude the render process
    wmic process where caption="msedge.exe" get name,commandline,processid|grep -vi "renderer"