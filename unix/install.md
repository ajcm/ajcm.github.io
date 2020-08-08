# Install Software

### Misc
	sudo apt install git curl wget -y

### NodeJs and NPM
curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.11/install.sh | bash
nvm --version
	
nvm install node
node --version

### Docker 
sudo apt install docker.io -y
docker --version

#### service
sudo systemctl enable docker
sudo systemctl start docker

##### group
```
sudo groupadd docker
sudo usermod -a -G  docker <user>
```
### Compose


```
curl -L https://github.com/docker/compose/releases/download/1.21.2/docker-compose-uname -s-uname -m -o docker-compose
sudo mv  ./docker-compose /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose


docker-compose --version
```

https://www.digitalocean.com/community/tutorials/how-to-install-docker-compose-on-ubuntu-18-04


### Homebrew
```
sh -c "$(curl -fsSL https://raw.githubusercontent.com/Linuxbrew/install/master/install.sh)"
	
test -d ~/.linuxbrew && eval $(~/.linuxbrew/bin/brew shellenv)
test -d /home/linuxbrew/.linuxbrew && eval $(/home/linuxbrew/.linuxbrew/bin/brew shellenv)
	
test -r ~/.bash_profile && echo "eval \$($(brew --prefix)/bin/brew shellenv)" >>~/.bash_profile
echo "eval \$($(brew --prefix)/bin/brew shellenv)" >>~/.profile
```

**eof**