## Echo "Hello CALLER"
The application is a simple HTTP flow listening on PORT 8081 and logging incoming requests and responds with "Hello CALLER"

![alt text](https://github.com/rezamt/docker-pack/blob/master/echo-mule/docs/echo-mule.png "Application Flow")


## Building Docker & Running 


```
docker build -t echo-mule .

```

## Running Container

```
docker run -d --name echo -p 8081:8081 -v /tmp/logs:/opt/mule/logs echo-mule

```

## Testing 

```
http GET  :8081/v1/echo

>>> Result

HTTP/1.1 200
Content-Length: 33
Content-Type: application/json
Date: Tue, 25 Apr 2017 06:04:59 GMT

{
    "message": "Hello CALLER"
}
```

## Logging
All of echo-mule container logs can be found under

```
ls -rtl /tmp/

-rw-r--r--  1 reza  wheel   5086 25 Apr 00:19 mule-app-classes.log
-rw-r--r--  1 reza  wheel   2368 25 Apr 00:23 mule-domain-default.log.2017-04-24
-rw-r--r--  1 reza  wheel  12381 25 Apr 00:23 mule-app-default.log.2017-04-24
-rw-r--r--  1 reza  wheel  34555 25 Apr 13:41 mule.log
-rw-r--r--  1 reza  wheel   5607 25 Apr 16:04 default.log
-rw-r--r--  1 reza  wheel   1184 25 Apr 16:04 mule-domain-default.log
-rw-r--r--  1 reza  wheel   8254 25 Apr 16:04 mule-app-default.log
-rw-r--r--  1 reza  wheel  37837 25 Apr 16:07 echo-mule.log

```
