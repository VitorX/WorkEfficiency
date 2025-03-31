## Description
    The XML element here is case sensitive, for example, if you replace 'EventData' with 'Eventdata', the query will not work.
    However the string in the value is case irrelevant. You can replace the 'App_pool_name' with 'APP_POOL_NAME'

## Filter Windows System event with IIS application pool name
    *[EventData[Data[@Name="AppPoolID"]="App_pool_name"]]

## Filter Windows Application event with specific URL or keywords contains in data element
    *[EventData[Data="http://aaa.bbb.ccc/ddd?eee=30"]]


## Filter with event with warning,error, critical and customizaed filer
    *[System[Provider[@Name='ASP.NET 4.0.30319.0'] and (Level=1  or Level=2 or Level=3)] and EventData[Data="C:\inetpub\wwwroot\my_apppool_name\"]]
