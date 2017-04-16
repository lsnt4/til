# How to Fix Laravel 'maximum column size' Error

Open `/config/database.php` and change `charset`, `collation` accordingly.

```diff
'mysql' => [
	'driver' => 'mysql',
	'host' => env('DB_HOST', '127.0.0.1'),
	'port' => env('DB_PORT', '3306'),
	'database' => env('DB_DATABASE', 'forge'),
	'username' => env('DB_USERNAME', 'forge'),
	'password' => env('DB_PASSWORD', ''),
	'unix_socket' => env('DB_SOCKET', ''),
-	'charset' => 'utf8mb4',
+	'charset' => 'utf8',
-	'collation' => 'utf8mb4_unicode_ci',
+	'collation' => 'utf8_unicode_ci',
	'prefix' => '',
	'strict' => true,
	'engine' => null,
],
```

### Resources:
[Stack Overflow](http://stackoverflow.com/a/42043927/3683435)
