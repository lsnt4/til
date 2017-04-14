# Access MySQL Databases From Host PC

Before starting the container, expose its internal port to host PC.

```shell
# docker run --restart always --name mysqlServer -p 33061:3306 -e MYSQL_ROOT_PASSWORD=mySuperSecretPassword -d mysql:latest
```

Now if you need you can create a PMA container as well (optional).

```shell
# docker run --restart always --name pma -d --link mysqlServer:db -p 1234:80 -e PMA_ARBITRARY=1 phpmyadmin/phpmyadmin
```

Once you get into the PMA login page, leave Server field blank and user name as `root` and password as `mySuperSecretPassword` or whatever you mentioned above. Since PMA container linked with MySQL container, it doesn't matter even if you ran a MySQL server on your local PC; PMA will automatically connect to the above linked container.

You can also log in to MySQL container by running **ONE** of following command, but if you use `localhost` instead of the IP, don't forget to include the protocol as well.
```shell
$ mysql -h 127.0.0.1 -P 33061 -u root -p
```
```shell
$ mysql -h localhost -P 33061 --protocol=tcp -u root -p
```