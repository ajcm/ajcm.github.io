# Linux misc

### SSH Folder permissions
```
#private key
chmod 600 id_rsa

#pub keys
chmod 644 .pub

# ~/.ssh
chmod 700 .shh
# home	
chmod 755 ~
```
	
	
### Tar exclude "node_modules"
```
tar  --exclude=**/node_modules/* --exclude=.git  -cvfz backup.tgz folder/
```

---