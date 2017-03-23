
Run a container without and with argument :

```
docker run hello-world
docker run docker/whalesay cowsay boo
```

List all the running images :

```
docker ps
```

List all the images that runned once :

```
docker ps -a
```

List all local images :

```
docker images

```

Delete a local image with his id :

```
docker rmi -f 48b5124b2768
```

To create our own image, create a file named Dockerfile in a directory :

```
FROM docker/whalesay:latest
RUN apt-get -y update && apt-get install -y fortunes
CMD /usr/games/fortune -a | cowsay
```

Then build it with a name (-t) and a position (.) :

```
docker build -t docker-whale .
```



