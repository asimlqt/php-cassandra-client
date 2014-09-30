## Installation

Using [composer](https://getcomposer.org/) is the recommended way to install it.

1 - Add "asimlqt/php-cassandra-client" as a dependency in your project's composer.json file.

```json
{
    "require": {
        "asimlqt/php-cassandra-client": "0.2.*"
    }
}
```

2 - Download and install Composer.

```
curl -sS https://getcomposer.org/installer | php
```

3 - Install your dependencies.

```
php composer.phar install
```

4 - Require Composer's autoloader.

```
require 'vendor/autoload.php';
```

## Usage

```php
$connection = new Cassandra\Cql\Connection("127.0.0.1:9042", "mykeyspace");

$query = "select * from mytable";
$result = $connection->query($query);

foreach($result as $row) {
    print_r($row);
}
```