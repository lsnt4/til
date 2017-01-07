# Compress Files with 7Zip

Installation
```shell
$ apt install p7zip-full
```

Compressing

```shell
$ 7z a -mx=9 archive_name.7z sql_file.sql
```
> `a` - Create archive  
> `-mx=9` - Ultra compression

### Notes:
* `-mx=9` or Ultra Compression may take long time to complete the process.

### Resources:
```shell
$ man 7z
```