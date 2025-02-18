
## Send HTTP Request with connection close

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

## Send HTTP Request without connection close
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

## Listen a port
    nc -l -p 1313

## Using -C for Send CRLF as line-ending.
By Default to use below command to get http request from apache web server will cause 400 error. After typing "GET /index.html HTTP/1.1" and press "enter" on the keyboard, the HTTP response will sendback immediately.

    fei@DESKTOP-BV7JE7U:~$ nc  localhost 80
    GET /index.html HTTP/1.1
    HTTP/1.1 400 Bad Request
    Date: Tue, 10 Sep 2024 03:24:43 GMT
    Server: Apache/2.4.52 (Ubuntu)
    Content-Length: 308
    Connection: close
    Content-Type: text/html; charset=iso-8859-1

    <!DOCTYPE HTML PUBLIC "-//IETF//DTD HTML 2.0//EN">
    <html><head>
    <title>400 Bad Request</title>
    </head><body>
    <h1>Bad Request</h1>
    <p>Your browser sent a request that this server could not understand.<br />
    </p>
    <hr>
    <address>Apache/2.4.52 (Ubuntu) Server at DESKTOP-BV7JE7U. Port 80</address>
    </body></html>

Working one command is use '-C' or using printf

    ```
    printf "GET /index.html HTTP/1.1\r\nHost: localhost\r\n\r\n" | nc localhost 80
    ```
    
    ```
    fei@DESKTOP-BV7JE7U:~$ nc -C localhost 80
    GET / HTTP/1.1
    HOST:localhost

    HTTP/1.1 200 OK
    Date: Tue, 10 Sep 2024 03:28:38 GMT
    Server: Apache/2.4.52 (Ubuntu)
    Last-Modified: Thu, 28 Mar 2024 03:37:29 GMT
    ETag: "29af-614b03e292f36"
    Accept-Ranges: bytes
    Content-Length: 10671
    Vary: Accept-Encoding
    Content-Type: text/html

    <!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
    <html xmlns="http://www.w3.org/1999/xhtml">
    <!--
        Modified from the Debian original for Ubuntu
        Last updated: 2022-03-22
        See: https://launchpad.net/bugs/1966004
    -->
    ...
    ```