MyGeotab PHP API Client
======================

[![Build Status](https://travis-ci.org/geotab/mygeotab-php.svg?branch=master)](https://travis-ci.org/geotab/mygeotab-php)
[![Packagist](https://img.shields.io/packagist/dm/geotab/mygeotab-php.svg)](https://packagist.org/packages/geotab/mygeotab-php)

Summary
------------
Provides a PHP client that can easily make API requests to a MyGeotab server. Sample:

```php
$api = new Geotab\API("user@example.com", "password", "DatabaseName", "my.geotab.com");
$api->authenticate();

$api->call("Get", "Device", ["resultsLimit" => 1], function ($results) {
    var_dump($results);
}, function ($error) {
    var_dump($error);
});
```