tag: #Laravel 

caso a rota n exista

```php
Route::fallback(function(){

    return 'Não existe essa rota';

});
```