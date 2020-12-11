## Install Docker/Compose

### Docker (Ubuntu)
```
sudo apt install docker.io -y

sudo systemctl start docker
sudo systemctl enable docker

sudo docker --version

#add user to docker group
sudo groupadd docker
sudo usermod -a -G  docker <USER>

# Test
docker run hello-world
```

### Docker (AWS Linux2)
```
#Install docker
sudo yum update -y
sudo yum install -y docker
sudo usermod -aG docker ec2-user
docker --version

sudo systemctl start docker
sudo systemctl enable docker

#Test
docker run hello-world

```

### Compose
[Reference](https://docs.docker.com/compose/install/)
```
sudo curl -L "https://github.com/docker/compose/releases/download/1.27.4/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose

docker-compose -version
```

---