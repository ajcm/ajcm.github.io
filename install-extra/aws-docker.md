## Install AWS Linux Docker/Compose

### Docker
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

**Docker Compose same as Ubuntu**


---