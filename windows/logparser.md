
# Logpaser

## Group by IIS logs by the HTTP status code
    >logparser -i:W3C "select sc-status,count(*) from *.log group by sc-status"


## Group by IIS logs by the Request URL Path with HTTP Response status code '500'
    >logparser -i:W3C "select  cs-uri-stem,count(*) from *.log  where sc-status='500' group by cs-uri-stem"
