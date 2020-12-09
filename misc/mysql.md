Export:
```
mysqldump -u root -p --opt --all-databases > alldb.sql
mysqldump -u root -p --all-databases --skip-lock-tables > alldb.sql
```
Import:
```
mysql -u root -p < alldb.sql
```