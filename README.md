# PDOWrapper
Simple PHP PDO wrapper to handle MySQL databases easily

## How to use

Update config.php with you database info

Then use this simple code snippet as a guide

```php
<?php
include_once 'config.php';
include_once 'Database.php';

$db = new Database($config);

$db->query("SELECT * FROM users WHERE username = :username");

$db->bind(":username", "admin");

$db->execute();

print_r($db->single());
```
