Router with namespanse example:

```php

Route::set('api', 'api/<controller>/<action>')
    ->defaults(['namespace' => 'AU\\Controller\\Api\\']);

Route::set('route-with-dash', 'auction-<id>', ['id' => '[0-9]++'])
    ->defaults(['namespace' => 'AU\\Controller\\', 'controller' => 'Auction', 'action' => 'index']);
```


Add a loader to the composer:

```json

...
"autoload": {
  "psr-4": {
    "AU\\": ["application/classes", "tests/classes"]
  }
},
...

```