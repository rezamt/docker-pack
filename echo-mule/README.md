
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
