# Backup & Restore MySQL Databases

Backup

```shell
$ mysqldump -h localhost -P 33061 -u root -p databaseName > databaseName.sql
```

Restore

```shell
$ mysql -h localhost -P 33061 --protocol=tcp -u root -p newDatabase < backup.sql
```