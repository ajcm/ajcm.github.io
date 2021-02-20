## Connection
```
mysql --host=localhost --user=myname --password=password <mydb>
mysql -h localhost -u myname -p password <mydb>

```

## Misc
```
#import
mysqldump -u root -p --opt --all-databases > alldb.sql
mysqldump -u root -p --all-databases --skip-lock-tables > alldb.sql

#export
mysql -u root -p < alldb.sql
```

