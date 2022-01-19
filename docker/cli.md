## build
```
docker build -t jsimage .
```
## run
```
docker run --rm -it -p 8082:80 webserver
```
The -it switch allows me to stop the container using Ctrl-C from the command-line

The –rm switch ensures that the container is deleted once it has stopped

```
docker run --rm -e diameter=5.0 jsparam
```
-e 指定环境变量

## rmi
```
docker rmi
```
## garbage collection commands
```
docker container prune -f
docker volume prune -f
// only dangling images are removed.
docker image prune -f
// remove all unused images
docker image prune --all
```
