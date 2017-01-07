# Continuously Monitor a Process By a Specific User

```shell
$ watch -n 1 pgrep -u www-data -a curl
```

> `n` - Interval  
> `u` - User  
> `a` - Display process command line and ID
> `l` - Display process name and ID