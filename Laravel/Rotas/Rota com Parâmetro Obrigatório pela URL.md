tag: #Laravel 

Passando parametro pela URL,Assim se não passar parametro não funciona

```php
Route::get('/jogos/{name}', function($name){

    return view('jogos', ['NomeJogo'=>$name]);

});
```