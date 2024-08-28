# Microsoft Edge WebView2
## Enable net-export
    Add enviroment:
    WEBVIEW2_ADDITIONAL_BROWSER_ARGUMENTS
    Value:
    --log-net-log=%USERPROFILE%\Desktop\net-export.json --net-log-capture-mode=Everything

Refer document

[WebView2 browser flags](https://learn.microsoft.com/en-us/microsoft-edge/webview2/concepts/webview-features-flags?tabs=dotnetcsharp)