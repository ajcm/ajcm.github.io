## Docker commands

#### Check volumes

$ docker inspect -f '{{ .Mounts }}' containerid

$ docker run -it -v /tmp:/tmp ubuntu:14.04 /bin/bash



#### show host ip

echo "$(ip -4 addr show docker0 | grep -Po 'inet \K[\d.]+')"




*eof*
