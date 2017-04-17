# Obtain The Contents of A HTML Element

Open `/config/database.php` and change `charset`, `collation` accordingly.

```php
<?php

	$doc = new DOMDocument();
	libxml_use_internal_errors(true);
	$doc->loadHTML($htmlDocument);
	$finder = new DomXPath($doc);
	$node = $finder->query("//*[contains(@class, 'className')]");
	print_r($doc->saveHTML($node->item(0)));

?>
```

### Source:
[Stack Overflow](http://stackoverflow.com/a/18316255/3683435)
