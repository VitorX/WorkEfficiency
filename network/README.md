# Network Tools

## WireShark

### Filters

Filter By IP address and 'HTTP' protocal and the keyword

    IPv4.Address == 10.110.70.10 && http && Description.Contains("index.html")

## Microsoft Network Monitor 

### Filters

Filter By IP address and 'HTTP' protocal and the keyword
    
    ip.addr==10.110.70.10 &&http && frame contains "theme"

## Netcat

### Send HTTP Request with connection close

    nc www.msftconnecttest.com 80
    GET http://www.msftconnecttest.com/connecttest.txt HTTP/1.1
    Connection: Close
    User-Agent: Microsoft NCSI
    Host: www.msftconnecttest.com

    # ------
    # Response
    # ------
    HTTP/1.1 200 OK
    Content-Length: 22
    Date: Thu, 05 Sep 2024 01:55:20 GMT
    Connection: close
    Content-Type: text/plain
    Cache-Control: max-age=30, must-revalidate

    Microsoft Connect Test

### Send HTTP Request without connection close
    nc www.msftconnecttest.com 80
    GET http://www.msftconnecttest.com/connecttest.txt HTTP/1.1
    User-Agent: Microsoft NCSI
    Host: www.msftconnecttest.com

    # ------
    # Response
    # ------
    HTTP/1.1 200 OK
    Content-Length: 22
    Date: Thu, 05 Sep 2024 01:55:57 GMT
    Connection: keep-alive
    Content-Type: text/plain
    Cache-Control: max-age=30, must-revalidate

    Microsoft Connect Test

### Listen a port
    nc -l -p 1313

