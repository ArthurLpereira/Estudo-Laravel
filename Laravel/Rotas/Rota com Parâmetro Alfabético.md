tag: #Laravel 

 Assim só aceita parametro com letras

```php
Route::get('/jogos/{name?}', function($name = null){

    return view('jogos', ['NomeJogo'=>$name]);

})->where('name', '[A-Za-z]+');
```