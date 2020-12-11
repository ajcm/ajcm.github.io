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

### Install Java
[Install Java Runtime Environment (JRE)](https://ubuntu.com/tutorials/install-jre#1-overview)

[How To Install Java with Apt on Ubuntu 18.04](https://www.digitalocean.com/community/tutorials/how-to-install-java-with-apt-on-ubuntu-18-04)
```
sudo apt install openjdk-8-jre -y
java -version

## Oracle JDK
(download)
sudo mkdir /usr/local/java
sudo mv jre-8u151-linux-x64.tar.gz /usr/local/java
cd /usr/local/java
sudo tar zxvf jre-8u151-linux-x64.tar.gz
sudo update-alternatives --install "/usr/bin/java" "java" "/usr/local/java/jre1.8.0_151/bin/java" 1

java -version
```

**Manage versions**

```
sudo update-alternatives --config java
```

### Install Gradle (custom version)
[How to Install Gradle on Ubuntu 18.04](https://linuxize.com/post/how-to-install-gradle-on-ubuntu-18-04/)

```
wget https://services.gradle.org/distributions/gradle-5.0-bin.zip -P /tmp
sudo unzip -d /opt/gradle /tmp/gradle-*.zip
ls /opt/gradle/gradle-5.0
```
**Setup environment variables**

```
sudo nano /etc/profile.d/gradle.sh
add:
	export GRADLE_HOME=/opt/gradle/gradle-5.0
	export PATH=${GRADLE_HOME}/bin:${PATH}
```

```
sudo chmod +x /etc/profile.d/gradle.sh
source /etc/profile.d/gradle.sh
```



### Homebrew
```
sh -c "$(curl -fsSL https://raw.githubusercontent.com/Linuxbrew/install/master/install.sh)"
	
test -d ~/.linuxbrew && eval $(~/.linuxbrew/bin/brew shellenv)
test -d /home/linuxbrew/.linuxbrew && eval $(/home/linuxbrew/.linuxbrew/bin/brew shellenv)
	
test -r ~/.bash_profile && echo "eval \$($(brew --prefix)/bin/brew shellenv)" >>~/.bash_profile
echo "eval \$($(brew --prefix)/bin/brew shellenv)" >>~/.profile
```

---