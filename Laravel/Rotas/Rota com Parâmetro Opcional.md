tag: #Laravel 

Aceita ou não um parâmetro passado pela URL.

```php
Route::get('/jogos/{name?}', function($name = null){

    return view('jogos', ['NomeJogo'=>$name]);

});
```