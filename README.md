# rebasedata-php-client


Installation via Composer
-------------------------

The recommended method to install is through [Composer](http://getcomposer.org).

1. Add `rebasedata/php-client` as a dependency in your project's `composer.json`:

    ```json
    {
        "require": {
            "rebasedata/php-client": "*"
        }
    }
    ```

2. Download and install Composer:

    ```bash
    curl -s http://getcomposer.org/installer | php
    ```

3. Install your dependencies:

    ```bash
    php composer.phar install
    ```

4. Require Composer's autoloader

    Composer also prepares an autoloader file that helps to autoload the libraries it downloads. To use it, just add the following line to your application:

    ```php
    <?php

    require 'vendor/autoload.php';

    use RebaseData\Client;

    $client = new Client('customerKey');
    ```
You can find out more about Composer at [getcomposer.org](http://getcomposer.org).


Example
-------

The following code is an example on how to convert a Microsoft Access ACCDB file to a ZIP-archive of CSV files.

```php
$inputFiles = ['/tmp/access.accdb'];
$outputFile = '/tmp/output.zip';

$client->convertAndReceiveZip($inputFiles, $outputFile);

echo "Conversion successful, check out /tmp/output.zip!\n";
```


License
-------

This code is licensed under the [MIT license](https://opensource.org/licenses/MIT).
