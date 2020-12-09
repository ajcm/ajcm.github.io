# Linux misc

### SSH Folder permissions

**Permissions**

.ssh directory: **700**
public key (.pub file): **644** 
private key (id_rsa): **600** 
home directory: **755**

```
chmod 700 .shh
chmod 644 .pub
chmod 600 id_rsa
	
chmod 755 ~
```
	
	
### Tar exclude "node_modules"

```
tar  --exclude=**/node_modules/* --exclude=.git  -cvfz backup.tgz folder/

```
---