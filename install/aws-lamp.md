## Install AWS Ec2

[Tutorial: Install a LAMP web server on Amazon Linux 2 ](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-lamp-amazon-linux-2.html)

### document root settings

```
sudo usermod -a -G apache ec2-user

sudo chown -R ec2-user:apache /var/www
sudo chmod 2775 /var/www && find /var/www -type d -exec sudo chmod 2775 {} \;
find /var/www -type f -exec sudo chmod 0664 {} \;

```

```
## Configure public_html
enable mod usedir
mkdir public_html
chmod 711 ~
chmod 755 ~/public_html
```

---