# Force APT to Use IPv4 Instead of IPv6 on Ubuntu

```shell
$ sudo apt-get -o Acquire::ForceIPv4=true update
$ sudo apt-get -o Acquire::ForceIPv4=true upgrade
$ sudo apt-get -o Acquire::ForceIPv4=true install git
```

To make this change permenent

```shell
$ sudo echo 'Acquire::ForceIPv4 "true";' | tee /etc/apt/apt.conf.d/99force-ipv4
```