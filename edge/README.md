# Microsoft Edge WebView2
## Enable net-export
    Add enviroment:
    WEBVIEW2_ADDITIONAL_BROWSER_ARGUMENTS
    Value:
    --log-net-log=%USERPROFILE%\Desktop\net-export.json --net-log-capture-mode=Everything

Refer document

[WebView2 browser flags](https://learn.microsoft.com/en-us/microsoft-edge/webview2/concepts/webview-features-flags?tabs=dotnetcsharp)


## Downgrade Edge Stable version
### Add following registry and repace the Edge version "132.0.2957.140" with yours
    reg add "HKLM\SOFTWARE\Policies\Microsoft\EdgeUpdate" /v "UpdateDefault" /t REG_DWORD /d 2 /f

    reg add "HKLM\SOFTWARE\Policies\Microsoft\EdgeUpdate" /v "RollbackToTargetVersion{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}" /t REG_DWORD /d 1 /f

    reg add "HKLM\SOFTWARE\Policies\Microsoft\EdgeUpdate" /v "TargetVersionPrefix{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}" /t REG_SZ /d "132.0.2957.140" /f
### Access Edge://settings/help to manually update the Edge

### Remove the registry after test
    reg delete "HKLM\SOFTWARE\Policies\Microsoft\EdgeUpdate" /v "UpdateDefault" /f

    reg delete "HKLM\SOFTWARE\Policies\Microsoft\EdgeUpdate" /v "RollbackToTargetVersion{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}" /f

    reg delete "HKLM\SOFTWARE\Policies\Microsoft\EdgeUpdate" /v "TargetVersionPrefix{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}" /f

## Downgrade Edge Beta version
### Add following registry and repace the Edge version "132.0.2957.140" with yours
    reg add "HKLM\SOFTWARE\Policies\Microsoft\EdgeUpdate" /v "UpdateDefault" /t REG_DWORD /d 2 /f
    reg add "HKLM\SOFTWARE\Policies\Microsoft\EdgeUpdate" /v "RollbackToTargetVersion{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}" /t REG_DWORD /d 1 /f
    reg add "HKLM\SOFTWARE\Policies\Microsoft\EdgeUpdate" /v "TargetVersionPrefix{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}" /t REG_SZ /d "134.0.3124.19" /f
### Access Edge://settings/help to manually update the Edge

### Remove the registry after test
    reg delete "HKLM\SOFTWARE\Policies\Microsoft\EdgeUpdate" /v "UpdateDefault" /f
    reg delete "HKLM\SOFTWARE\Policies\Microsoft\EdgeUpdate" /v "RollbackToTargetVersion{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}" /f
    reg delete "HKLM\SOFTWARE\Policies\Microsoft\EdgeUpdate" /v "TargetVersionPrefix{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}" /f
