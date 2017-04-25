## Dockerfile for Mule Standalone ESB

Based on java:8 with Mule ESB 3.8.1 (installed in /opt/mule)


## Building Docker Mule Standalone 3.8.1

```
docker build -t mule-standalone:3.8.1 .

```
## Deploying your Mule Application to the runtime environment

```
docker run -d --name DOCKER_NAME -p 8081:8081 -v /somewhere/where/myapps/is:/opt/mule/apps -v /somewhere/where/iwanttolog:/opt/mule/logs codingtony/mule

e.g. 
docker run -d --name echo-mule -p 8081:8081 -v /tmp/echo-mule:/opt/mule/apps/echo-mule -v /tmp/logs:/opt/mule/logs mule-standalone:3.8.1

```

## Startup and Shutdown Script

$MULE_HOME/bin/mule status|stop|Start|restart|dump|console


## Passing Parameters to the JVM via the Startup Command
$MULE_HOME/bin/mule start -D-Mmule.mmc.bind.port=7783-7883


## Use it with your Mule application

### Use it with your Mule application
| important directories | description
|--- |---
|/opt/mule/apps | Application directory
|/opt/mule/conf | Configuration & log4j configuration. wrapper.conf is mandatory
|/opt/mule/logs | Log files
|/opt/mule/domains | Domains directory

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

