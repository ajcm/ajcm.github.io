## Docker commands

### Images

Image name format
```
<docker-id>/<project-repo>:<tag> (default tag: 'lastest') 
```

Create image:
````
docker build -t <image> .
```

Pull/push images from repository:
```
docker pull <image>
docker push <image>
```

Import/export images:
```
docker load -i <path to image>
docker save -o <path to tarfile> <image>
```

List and inspect images
```
docker inspect <image>
docker image list
```
### Containers
Docker run creates a new container from a image and executes it.

```
docker run <options> <image> --name <container name>
  
options:
 --rm removes container after finish
 -d detach/daemon
 -it interactive + terminal 

mappings:
 -p <host port>:<container port>
 -v <host folder>:<container folder>
```

Create, start and stop:
```
docker create <image> --name <container name>

docker start/stop <options> <container id/name>
options:
 -a appends output/stderr
```

Check logs, send SIGTERM and SIGKILL
```
docker logs <container>
docker stop <container>
docker kill <container>
```
Execute commands on running container
```
docker exec <-it> <container> <command>
```
Commit container to image
```
docker commit <options> <container> <image>
options:
 -c execute docker file command on image
````

### Other
**Check volumes**
```
$ docker inspect -f '{{ .Mounts }}' containerid
$ docker run -it -v /tmp:/tmp ubuntu:14.04 /bin/bash
```

**Show host ip**
```
echo "$(ip -4 addr show docker0 | grep -Po 'inet \K[\d.]+')"
```
### References

[Exploring Docker container's file systemn](https://sites.google.com/site/javabitdotnet/docker-1/docker-image-inspection)

---