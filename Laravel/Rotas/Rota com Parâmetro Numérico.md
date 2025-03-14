tag: #Laravel 

Assim só aceita numérico

```php
Route::get('/jogos/{name?}', function($name = null){

    return view('jogos', ['NomeJogo'=>$name]);

})->where('name', '[0-9]+');
```