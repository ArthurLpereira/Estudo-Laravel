tag: #Laravel 

 Redirecionamento por rotas. Nomenclatura é muito importante pois mesmo se mudar o caminho o nome continua o mesmo, então n tem q mudar no html

```php
Route::get('/', function () {

    return view('welcome');

})->name('home-index');

  

Route::view('/jogos', 'jogos');
```
