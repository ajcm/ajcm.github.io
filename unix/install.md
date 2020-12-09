## Install Software (Ubuntu)

### Misc
```
sudo apt install git curl wget -y
```

### NodeJs and NPM (with NVM)
[Easy way to install nvm on Ubuntu 18.04](https://nbanzyme.medium.com/easy-way-to-install-nvm-on-ubuntu-18-04-2cfb19ee5391)
```
curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.11/install.sh | bash
nvm --version
	
nvm install node
node --version
```




### Homebrew
```
sh -c "$(curl -fsSL https://raw.githubusercontent.com/Linuxbrew/install/master/install.sh)"
	
test -d ~/.linuxbrew && eval $(~/.linuxbrew/bin/brew shellenv)
test -d /home/linuxbrew/.linuxbrew && eval $(/home/linuxbrew/.linuxbrew/bin/brew shellenv)
	
test -r ~/.bash_profile && echo "eval \$($(brew --prefix)/bin/brew shellenv)" >>~/.bash_profile
echo "eval \$($(brew --prefix)/bin/brew shellenv)" >>~/.profile
```

**eof**