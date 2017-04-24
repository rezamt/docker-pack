#Dockerfile for Mule Standalone ESB

Based on java:8 with Mule ESB 3.8.1 (installed in /opt/mule)


##Building Docker Mule Standalone 3.8.1

```
docker build -t mule-standalone:3.8.1 .

```

## Checking Docker image

Access your built image and see how it's built

```
docker run -it mule-standalone:3.8.1 bash

```


## Use it with your Mule application

  Directories           | Description
     
1|/opt/mule/apps         | Application directory
2|/opt/mule/conf         | Configuration & log4j configuration. wrapper.conf is mandatory
3|/opt/mule/logs         | Log files
4|/opt/mule/domains      | Domains directory


## Packaging Your Application



## Running Your Application on Docker

```
docker run -d -name YOUR-DOCKER-NAME -p 8888:8888 -v /somewhere/where/myapps/is:/opt/mule/apps -v /somewhere/where/iwanttolog:/opt/mule/logs mule-standalone:3.8.1

````

To check the stdout :
```
docker logs YOUR-DOCKER-NAME
```

To stop the container :
```
docker kill YOUR-DOCKER-NAME
```

