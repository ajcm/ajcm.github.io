## Install AWS Ec2

### Misc
```
sudo yum update -y
sudo yum install git curl wget -y

```

### Lamp
[AWS Installation](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-lamp-amazon-linux-2.html)
```
sudo amazon-linux-extras install -y lamp-mariadb10.2-php7.2 php7.2 -y
sudo yum install -y httpd mariadb-server -y

sudo systemctl start httpd
sudo systemctl enable httpd
sudo systemctl is-enabled httpd
```

### NodeJs
```
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.34.0/install.sh | bash
nvm install node
node -e "console.log('Running Node.js ' + process.version)"
```

### Install Java (Amazon Correcto)
[AWS Correcto](https://docs.aws.amazon.com/corretto/latest/corretto-11-ug/amazon-linux-install.html)
```
sudo yum install java-11-amazon-corretto -y

sudo alternatives --config java
```
---