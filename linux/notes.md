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

# remove or change password from key
 ssh-keygen -p
 
 ssh-keygen -p [-P old_passphrase] [-N new_passphrase] [-f keyfile]
 
```
	
	
### Tar exclude "node_modules"
```
tar  --exclude=**/node_modules/* --exclude=.git  -cvfz backup.tgz folder/
```

---