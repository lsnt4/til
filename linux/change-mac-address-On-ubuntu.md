# Change MAC Address on Ubuntu

```shell
$ sudo ifconfig eth0 down
$ sudo ifconfig eth0 hw ether XX:XX:XX:XX:XX:XX
$ sudo ifconfig eth0 up
```