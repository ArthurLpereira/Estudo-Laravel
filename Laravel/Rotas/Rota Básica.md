tag: #Laravel 

Essa rota é a basica, se a url for / ela vai puxar a view welcome

```php
Route::get('/', function () {

    return view('welcome');
});
```
