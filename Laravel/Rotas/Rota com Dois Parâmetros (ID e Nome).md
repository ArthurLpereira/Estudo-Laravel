tag: #Laravel 

Passando dois parâmetros um numérico e um alfabético

```php
Route::get('/jogos/{id?}/{name?}', function($name = null, $id = null){

    return view('jogos', ['NomeJogo'=>$name, 'IdJogo'=>$id]);

})->where('name', '[A-Za-z]+','id', '[0-9]+' );
```